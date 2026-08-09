---
name: Sarj
description: Use when building outbound voice call automation, integrating voice AI agents into applications, tracking call outcomes, or processing speech (transcription and synthesis). Reach for this skill when users ask to make calls, check call status, configure webhooks, or work with speech APIs.
metadata:
    mintlify-proj: sarj
    version: "1.0"
---

# Sarj.ai Skill

## Product summary

Sarj.ai is a REST API and MCP server for outbound voice calls with AI agents. It handles call placement, call tracking, transcription, and speech synthesis for conversational AI applications. The platform supports Arabic, English, and Urdu with low-latency speech processing.

**Key endpoints:**
- `POST /api/v1/calls` — Place an outbound call
- `GET /api/v1/calls/{call_id}` — Fetch call details, transcript, recording, and outcome report
- `POST /api/v1/health` — Health check (no auth required)

**Key files and config:**
- API key: Generate at `https://platform.sarj.ai/api-keys` (shown once; store as `SARJ_API_KEY` env var)
- Scenario ID: Create at `https://platform.sarj.ai/scenarios` (prefixed `scn_`)
- Webhook URL: Configure in dashboard (one per organization)

**SDKs and clients:**
- Python SDK: `pip install sarj-platform-sdk`
- MCP Server: `https://platform-api.sarj.ai/api/v1/mcp` (OAuth auto-auth)
- REST API: `https://platform-api.sarj.ai/api/v1`

**Primary docs:** https://platform-docs.sarj.ai

## When to use

Reach for this skill when:
- A user asks to make a phone call, dial a number, or trigger an outbound call
- You need to check call status, retrieve transcripts, or download recordings
- You're setting up call webhooks for real-time notifications
- You need to transcribe audio (Speech-to-Text) or generate speech (Text-to-Speech)
- You're integrating Sarj.ai into an MCP-compatible agent (Claude Code, Cursor)
- You need to pass template variables into a scenario or set call language

Do not use this skill for:
- Inbound call handling (Sarj.ai is outbound-only)
- Modifying or creating scenarios (use the dashboard)
- Generating API keys (dashboard only)

## Quick reference

### Call placement

| Task | Method | Required fields |
|------|--------|-----------------|
| Place a call | `POST /api/v1/calls` | `phone_number` (E.164), `scenario_id` (scn_*) |
| Fetch call details | `GET /api/v1/calls/{call_id}` | `call_id` |
| Health check | `GET /api/v1/health` | None (no auth) |

### Call status progression

```
queued → in_progress → completed
                    ↓
              (or failed/timeout/user_rejected/voicemail)
```

### Call response fields

| Field | Type | Notes |
|-------|------|-------|
| `id` | string | Unique call identifier |
| `status` | enum | queued, in_progress, completed, failed, etc. |
| `phone_number` | string | E.164 format |
| `scenario_id` | string | scn_-prefixed ID |
| `recording_url` | string | Signed, time-limited download link |
| `transcript` | array | List of {role, content} objects (user/assistant) |
| `report` | object | Outcome assessment with success criteria (async, ~2 min) |
| `duration` | integer | Seconds (null until call ends) |
| `language` | enum | en, ar, ur |

### MCP tools

| Tool | Purpose |
|------|---------|
| `createCall` | Place outbound call (POST /calls) |
| `getCall` | Fetch call details (GET /calls/{call_id}) |

### Speech APIs

| API | Endpoint | Purpose |
|-----|----------|---------|
| STT | `POST https://stt-rnnt-ar.sarj.ai/openai/v1/audio/transcriptions` | Transcribe audio to text |
| TTS | `POST https://sarj-omni-tts.sarj.ai/v1/audio/speech` | Generate speech from text |

## Decision guidance

### When to use REST API vs MCP Server

| Scenario | Use REST API | Use MCP Server |
|----------|-------------|----------------|
| Direct backend integration | ✓ | |
| Python/Node.js application | ✓ | |
| Claude Code / Cursor agent | | ✓ |
| Batch call automation | ✓ | ✓ |
| Manual API key management | ✓ | |
| OAuth auto-auth preferred | | ✓ |

### When to poll vs use webhooks

| Scenario | Poll | Webhook |
|----------|------|---------|
| Single call, wait for result | ✓ | |
| Batch calls, real-time updates | | ✓ |
| Asynchronous processing | | ✓ |
| Simple synchronous flow | ✓ | |
| High-volume calls | | ✓ |

**Note:** Reports are generated asynchronously (~2 min after completion). Polling alone is insufficient for production; use webhooks as the authoritative source.

### When to use Speech APIs

| Task | API | Notes |
|------|-----|-------|
| Transcribe call recording | STT | OpenAI-compatible |
| Generate voice from text | TTS | Supports voice cloning |
| Real-time transcription | STT | Streaming supported |
| Custom voice synthesis | TTS | Clone endpoint available |

## Workflow

### Typical call workflow

1. **Verify setup:** Call `GET /api/v1/health` to confirm API is reachable (no auth required).

2. **Prepare call parameters:**
   - Phone number in E.164 format (e.g., `+966512345678`)
   - Scenario ID from dashboard (starts with `scn_`)
   - Optional: template variables (dict), language (en/ar/ur, defaults to ar)

3. **Place the call:** POST to `/api/v1/calls` with phone_number, scenario_id, and optional variables/language. Returns `call_id` and initial status (queued).

4. **Track the call:** Either:
   - **Poll:** Repeatedly call `GET /api/v1/calls/{call_id}` until status is terminal (completed, failed, etc.)
   - **Webhook:** Configure webhook URL in dashboard; Sarj.ai POSTs when call ends

5. **Retrieve results:** Once completed, response includes:
   - `recording_url` (signed, time-limited)
   - `transcript` (array of user/assistant messages)
   - `report` (outcome assessment, generated ~2 min after completion)

6. **Handle async report:** If report is null immediately after completion, poll again or wait for webhook. Reports only exist for completed/max_duration_reached calls.

### Setting up webhooks

1. Prepare an HTTPS endpoint that:
   - Returns 2xx within 10 seconds
   - Is idempotent (deduplicates on `call_id`)
   - Handles retries (up to 3 attempts, 2-sec delay)

2. Set webhook URL in Sarj.ai Dashboard (one per organization).

3. Test with "Send test webhook" button in dashboard.

4. Verify with a real test call.

### Using MCP Server with Claude Code

1. Add server: `claude mcp add sarj-voice --transport http https://platform-api.sarj.ai/api/v1/mcp`

2. On first use, browser opens Sarj.ai sign-in; API key is cached automatically.

3. Prompt agent: "Call +966512345678 using scenario scn_appointment_reminder with language set to Arabic."

4. Agent uses `createCall` and `getCall` tools natively.

## Common gotchas

- **API key shown once:** Copy and store immediately as env var. If lost, generate a new one from dashboard.

- **Phone number format:** Must be E.164 (leading +, country code, no spaces/dashes). `+966512345678` ✓, `966512345678` ✗, `+966 51 234 5678` ✗

- **Scenario ID required:** Cannot place a call without a valid `scn_`-prefixed scenario ID. Create scenarios in dashboard first.

- **Report is async:** The `report` field is null immediately after call completion. It appears ~2 minutes later. Polling alone is unreliable; use webhooks for production.

- **Recording URL is time-limited:** Download promptly or fetch a fresh URL via `GET /calls/{call_id}`.

- **Webhook must be idempotent:** Same `call_id` may arrive multiple times if your response is delayed. Deduplicate on `call_id`.

- **Language defaults to Arabic:** If not specified, calls default to `ar`. Explicitly set `language: "en"` or `"ur"` if needed.

- **Call limits per phone number:** Hitting a per-number rate limit returns 429 with `call_limit_exceeded` error. Check error.call_limit field.

- **Blocked phone numbers:** Some numbers may be blocked; error type is `phone_number_blocked`.

- **Webhook signature verification not yet shipped:** For now, secure webhooks via IP allow-listing (contact support) or hard-to-guess URL path.

- **Speech APIs are separate base URLs:** STT and TTS use different endpoints and require the same API key.

## Verification checklist

Before submitting work:

- [ ] API key is stored securely (env var, not hardcoded)
- [ ] Phone numbers are in E.164 format
- [ ] Scenario ID is valid and accessible (starts with `scn_`)
- [ ] Health check passes: `GET /api/v1/health` returns `{"data": {"status": "ok"}}`
- [ ] Call placement returns 202 Accepted with a valid `call_id`
- [ ] Call status progresses through expected states (queued → in_progress → completed)
- [ ] Webhook endpoint (if used) returns 2xx within 10 seconds
- [ ] Webhook endpoint is idempotent (deduplicates on `call_id`)
- [ ] Recording URL is downloaded before it expires
- [ ] Transcript and report are retrieved (report may take ~2 min)
- [ ] Error responses branch on `error.type`, not `message`
- [ ] Request IDs are logged for support tickets

## Resources

**Comprehensive page listing:** https://platform-docs.sarj.ai/llms.txt

**Critical documentation:**
- [Getting Started](https://platform-docs.sarj.ai/getting-started) — API key, health check, first call
- [API Reference](https://platform-docs.sarj.ai/api-reference) — Interactive endpoint docs with schemas
- [MCP Server](https://platform-docs.sarj.ai/mcp-server) — Connect Claude Code, Cursor, or MCP-compatible agents
- [Webhooks](https://platform-docs.sarj.ai/webhooks) — Configure push notifications for call completion

---

> For additional documentation and navigation, see: https://platform-docs.sarj.ai/llms.txt