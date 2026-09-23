---
name: Sarj
description: Use when placing outbound voice calls, tracking call status and transcripts, managing scheduled calls with retries, or integrating voice AI into applications. Agents should reach for this skill when users request voice calling, need to retrieve call recordings/transcripts, configure retry policies, or work with the MCP server for agent-native call tools.
metadata:
    mintlify-proj: sarj
    version: "1.0"
---

# Sarj.ai Skill

## Product Summary

Sarj.ai is a REST API and MCP server for placing and managing outbound voice calls. Agents use it to dial phone numbers, run AI scenarios, track call progress, retrieve recordings and transcripts, and configure retry policies. The platform supports multiple languages (Arabic, English, Urdu) and integrates with Claude Code, Cursor, and any MCP-compatible client via the MCP server at `https://platform-api.sarj.ai/api/v1/mcp`. Key endpoints: `POST /api/v1/calls` (place call), `GET /api/v1/calls/{call_id}` (fetch details), `POST /api/v1/schedule-configs` (create retry policy). Use the Python SDK (`pip install sarj-platform-sdk`) or REST API with Bearer token authentication. Primary docs: https://platform-docs.sarj.ai

## When to Use

- **Place outbound calls**: User asks to call, dial, ring, or phone someone; use `POST /calls` with phone number and scenario ID
- **Track call status**: User asks about a specific call's progress, transcript, or recording; use `GET /calls/{call_id}`
- **Retrieve recordings/transcripts**: User needs the call recording URL or conversation text; fetch via `GET /calls/{call_id}` and use `permanent_recording_url` (does not expire)
- **Configure retries**: User wants automatic retry on no-answer; create a schedule config via `POST /schedule-configs` and reference it when placing calls
- **Schedule future calls**: User wants to dial at a specific time; use `scheduled_at` parameter (10 minutes to 30 days ahead)
- **Cancel/reschedule pending calls**: User wants to stop or move a scheduled call; use `DELETE /calls/{call_id}` or `PATCH /calls/{call_id}` while status is `scheduled`
- **Receive webhooks**: User wants push notifications when calls complete; configure webhook URL in dashboard (one per organization)
- **MCP integration**: User is working in Claude Code, Cursor, or MCP-compatible agent; use MCP server for native `createCall` and `getCall` tools

## Quick Reference

### API Endpoints

| Endpoint | Method | Purpose |
|----------|--------|---------|
| `/health` | GET | Health check (no auth required) |
| `/calls` | POST | Place outbound call |
| `/calls/{call_id}` | GET | Fetch call details |
| `/calls/{call_id}` | DELETE | Cancel pending scheduled call |
| `/calls/{call_id}` | PATCH | Reschedule pending call |
| `/schedule-configs` | POST | Create retry policy |

### Call Status States

| Status | Meaning |
|--------|---------|
| `queued` | Waiting to dial |
| `in_progress` | Call is active |
| `completed` | Call finished, report available |
| `scheduled` | Booked for future time |
| `no_answer` | Rang, no pickup |
| `user_rejected` | Customer hung up or busy |
| `failed` | Telephony failure |
| `cancelled` | Manually cancelled |
| `expired` | Scheduled call expired before dialing |

### Authentication

All requests (except `/health`) require Bearer token in `Authorization` header:
```
Authorization: Bearer YOUR_API_KEY
```

Get API key from https://platform.sarj.ai/api-keys (shown only once—store as env var `SARJ_API_KEY`).

### Call Parameters

| Parameter | Required | Notes |
|-----------|----------|-------|
| `phone_number` | Yes | E.164 format (e.g., `+966512345678`) |
| `scenario_id` | Yes | Scenario ID from dashboard (starts with `scn_`) |
| `language` | No | `en`, `ar`, `ur`; defaults to `ar` |
| `variables` | No | Template variables object for scenario |
| `scheduled_at` | No | RFC 3339 timestamp; 10 min to 30 days ahead |
| `schedule_config_id` | No | Retry policy ID from `POST /schedule-configs` |

### Response Format

All endpoints return standard envelope:
```json
{
  "data": { /* response payload */ },
  "meta": { "request_id": "..." }
}
```

Errors include `error.type` (branch on this, not message):
```json
{
  "error": {
    "type": "unauthorized",
    "message": "Authentication required."
  },
  "meta": { "request_id": "..." }
}
```

## Decision Guidance

| Scenario | Use | Why |
|----------|-----|-----|
| **Immediate call** | `POST /calls` without `scheduled_at` | Dials now, returns `call_id` immediately |
| **Future call** | `POST /calls` with `scheduled_at` | Dials at specified time, status `scheduled` until release |
| **Retry on no-answer** | Create `schedule_config`, reference in `POST /calls` | Automatic retries with configurable delay and window |
| **No retries** | Omit `schedule_config_id` | Uses scenario's default config (if any) |
| **Poll for updates** | `GET /calls/{call_id}` in loop | Synchronous, blocks until report available (2 min typical) |
| **Push updates** | Configure webhook in dashboard | Asynchronous, fires when call ends; must be idempotent |
| **Download recording** | Use `permanent_recording_url` from `GET /calls/{call_id}` | Does not expire; safe to store long-term |
| **Download recording (legacy)** | Use `recording_url` if `permanent_recording_url` is null | Expires in 24–7 days; fetch promptly |

## Workflow

1. **Verify API access**: Call `GET /health` to confirm API is reachable (no auth needed)
2. **Get API key**: Sign in at https://platform.sarj.ai/api-keys, generate key, store as `SARJ_API_KEY` env var
3. **Identify scenario**: Go to https://platform.sarj.ai/scenarios, find or create scenario, copy `scn_`-prefixed ID
4. **Place call**: POST to `/api/v1/calls` with `phone_number`, `scenario_id`, optional `language`, `variables`, `scheduled_at`, `schedule_config_id`
5. **Track progress**: Poll `GET /api/v1/calls/{call_id}` or configure webhook to receive updates
6. **Wait for report**: Report (success/failure against criteria) generated asynchronously, typically within 2 minutes of completion
7. **Retrieve data**: Extract `transcript`, `recording_url` or `permanent_recording_url`, and `report.outcome` from call detail
8. **Handle retries**: If call failed and retry config is set, platform automatically dials again; each attempt is a separate call with its own webhook

## Common Gotchas

- **API key shown once**: Copy immediately after generation; cannot be retrieved later. Store as env var.
- **Report is async**: `report` field is `null` immediately after call completes. Poll again or wait for webhook. Only `completed` and `max_duration_reached` statuses get reports; other terminal statuses never do.
- **Recording URLs expire**: `recording_url` expires in 24–7 days. Use `permanent_recording_url` (does not expire) if available; fall back to `recording_url` during rollout.
- **Webhook must be idempotent**: Same `call_id` may arrive multiple times if your 2xx response is delayed. Deduplicate on `call_id`.
- **Scheduled calls can only be cancelled/rescheduled while pending**: Once status changes from `scheduled` to anything else, cancel/reschedule returns 409. Check status before attempting.
- **Retry config is create-only**: No way to fetch, list, update, or delete after creation (ships in future release). Plan ahead.
- **Phone number format**: Must be E.164 (e.g., `+966512345678`). Invalid format returns validation error.
- **Scenario must exist and be accessible**: Scenario ID must be valid and your API key's organization must have access. Returns `scenario_not_found` or `scenario_forbidden` if not.
- **Language defaults to Arabic**: If not specified, `language` defaults to `ar`. Explicitly set `en` or `ur` if needed.
- **Webhook retries are automatic**: Platform retries failed webhook deliveries up to 3 times with 2-second delay. After 3 failures, delivery is marked failed but call data is durable (re-fetch via `GET /calls/{call_id}`).
- **Booking outcome on create**: Response includes `booking_outcome` field: `created` (new call), `rescheduled_existing` (took over existing pending call), or `kept_existing` (kept existing call). Check this to avoid assuming a second call exists.

## Verification Checklist

Before submitting work:

- [ ] API key is valid and stored securely (not in code)
- [ ] Phone number is in E.164 format (e.g., `+966512345678`)
- [ ] Scenario ID exists and starts with `scn_`
- [ ] Language parameter is one of `en`, `ar`, `ur` (or omitted for default `ar`)
- [ ] For scheduled calls: `scheduled_at` is 10+ minutes ahead and within 30 days
- [ ] For retries: Schedule config was created and `schedule_config_id` is referenced in call
- [ ] Webhook endpoint (if used) returns 2xx within 10 seconds and is idempotent
- [ ] Call was placed successfully (202 Accepted response with `call_id`)
- [ ] Call status is tracked via polling or webhook (not assumed to be complete immediately)
- [ ] Report is checked only after call reaches terminal state (not immediately after completion)
- [ ] Recording URL is `permanent_recording_url` if available; fall back to `recording_url` only if necessary
- [ ] Error responses are handled by branching on `error.type`, not parsing message text
- [ ] `meta.request_id` is logged for support tickets

## Resources

- **Comprehensive page listing**: https://platform-docs.sarj.ai/llms.txt
- **Getting Started**: https://platform-docs.sarj.ai/getting-started
- **API Reference**: https://platform-docs.sarj.ai/api-reference
- **MCP Server**: https://platform-docs.sarj.ai/mcp-server
- **Webhooks**: https://platform-docs.sarj.ai/webhooks

---

> For additional documentation and navigation, see: https://platform-docs.sarj.ai/llms.txt