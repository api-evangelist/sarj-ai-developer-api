---
name: sarj-scheduled-calls
description: Use when booking a Sarj.ai voice call for a future time, stopping a booked call or a pending retry chain, moving a booked call to a new time, or setting up a retry policy. Reach for this skill whenever the user wants a call to happen later, wants to stop calling someone, or asks how many times Sarj.ai will re-dial.
api: openapi/_original/sarj-ai-developer-api-developer-openapi.json
operations:
  - createCall
  - cancelScheduledCall
  - rescheduleScheduledCall
  - createScheduleConfig
  - getCall
generated: '2026-09-11'
method: generated
source: >-
  Grounded in openapi/_original/sarj-ai-developer-api-developer-openapi.json (fetched from
  https://platform-api.sarj.ai/api/v1/openapi.json on 2026-09-11). Every operationId, path, method, field
  name, status code and numeric bound below was read out of that document. Nothing here is invented.
---

# Sarj.ai — scheduled calls, cancellation and retries

This skill covers the deferred-execution half of the Sarj.ai call API: booking a call instead of dialing
now, and the two operations that let you take a booking back.

> **Correction to the provider's own skill.** Sarj.ai's published Agent Skill
> (`/.well-known/agent-skills/sarj/skill.md`) lists cancel as `DELETE /calls/{call_id}` and reschedule as
> `PATCH /calls/{call_id}`. The OpenAPI defines neither. The real operations are
> `POST /calls/{call_id}/cancel` and `POST /calls/{call_id}/reschedule`. Use the paths below.

## Why booking matters

`createCall` without `scheduled_at` dials immediately and **cannot be undone** — there is no abort, hang-up
or refund operation anywhere on the contract. `createCall` **with** `scheduled_at` creates the call in
status `scheduled` and leaves a window in which you can cancel or move it. If you are acting on someone's
behalf and want a way back, book the call rather than placing it.

## Operations

| operationId | Method + path | Notes |
|---|---|---|
| `createCall` | `POST /calls` | 202. `scheduled_at` must be ≥ 10 minutes ahead and ≤ 30 days out (RFC 3339 with offset). |
| `cancelScheduledCall` | `POST /calls/{call_id}/cancel` | 200 on success. 409 `call_not_pending` once released for dialing. |
| `rescheduleScheduledCall` | `POST /calls/{call_id}/reschedule` | Body `{ "scheduled_at": ... }`. 409 once released, 422 `invalid_schedule_time` if out of range. |
| `createScheduleConfig` | `POST /schedule-configs` | 201. Create-only — no read, list, update or delete exists. |
| `getCall` | `GET /calls/{call_id}` | Read `status` before attempting cancel or reschedule. |

## Booking a call

```
POST /api/v1/calls
Authorization: Bearer $SARJ_API_KEY
{
  "phone_number": "+966512345678",
  "scenario_id": "scn_abc123",
  "language": "ar",
  "scheduled_at": "2026-05-01T15:30:00+03:00",
  "schedule_config_id": "01890000-0000-7000-8000-000000000000"
}
```

Check `data.booking_outcome` on the 202 response. It is one of `created`, `rescheduled_existing` or
`kept_existing` — the last two mean Sarj.ai folded your request into a pending call that already existed,
so **do not assume a second call now exists**.

## Stopping a call

`cancelScheduledCall` is the per-person stop-calling lever. Cancelling a pending retry ends that retry
chain, so one call stops every remaining attempt against that number.

```
POST /api/v1/calls/{call_id}/cancel
Authorization: Bearer $SARJ_API_KEY
```

- `200` — cancelled.
- `409 call_not_pending` — the call was already released for dialing. This is terminal; do not retry.
  Read the returned `status` to see what it became.
- `403 scheduling_disabled` — scheduling is not enabled for this tenant. No request shape fixes this.

## Retry policies

```
POST /api/v1/schedule-configs
{
  "max_retries": 2,
  "wait_between": "PT2H",
  "retry_window": { "start_edge": {"hour": 9, "minute": 0}, "end_edge": {"hour": 20, "minute": 0} },
  "timezone": "Asia/Riyadh",
  "expire_after": "P3D"
}
```

Published bounds, straight from the schema: `max_retries` 1–10, `wait_between` 60 seconds to 30 days
(raw seconds or an ISO 8601 duration), `expire_after` 1 hour to 7 days. `retry_window` is a daily wall-clock
window evaluated in `timezone`.

**Treat this as irreversible.** The provider states there is no way to fetch, list, update or disable a
config after creation. Confirm the numbers with the user before you create one — a wrong `max_retries`
means a real person is dialed more times than they agreed to, and you cannot turn it off through the API.
You can create a config with `"enabled": false`, but you cannot flip that flag later.

## Rules that apply to every operation here

- **No idempotency.** No operation on this API accepts an `Idempotency-Key`. A timed-out `createCall` cannot
  be safely retried — it may have placed the call. Check with `getCall` before resending.
- **No rate-limit headers.** The only limit signal is a `429 call_limit_exceeded` body carrying the offending
  `phone_number` and the integer `call_limit`. There is no `Retry-After`.
- **Branch on `error.type`, never on `error.message`.** The error object is a discriminated union; the
  message is for humans. Full catalog: `errors/sarj-ai-developer-api-problem-types.yml`.
- **Correlate with `meta.request_id`** and send your own `X-Request-ID` — it is echoed on success and error.
- **Webhooks are authoritative.** A cancelled booking emits a `cancelled` webhook; an expired one emits
  `expired`. `next_retry_at: null` is the terminal signal for a contact, not the call status. See
  `asyncapi/sarj-ai-developer-api-webhooks.yml`.

## Verification checklist

- [ ] `scheduled_at` is ≥ 10 minutes ahead and ≤ 30 days out, RFC 3339 with a timezone offset.
- [ ] `booking_outcome` checked before assuming a new call was created.
- [ ] `getCall` status is `scheduled` before calling cancel or reschedule.
- [ ] 409 treated as terminal, not retried.
- [ ] Retry-policy numbers confirmed with the user before `createScheduleConfig`.
