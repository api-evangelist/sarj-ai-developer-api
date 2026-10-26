# Sarj AI Developer API (sarj-ai-developer-api)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Sarj.ai is a voice and chat AI agent platform built for Arabic, English and Urdu, focused on the Saudi and wider MENA market. The public developer surface is a REST API for outbound voice calls — place a call against a saved scenario, then retrieve its status, signed recording URL, transcript and asynchronous post-call outcome report. Alongside the call API, Sarj publishes two OpenAI-compatible speech APIs (Speech-to-Text with streaming, and Text-to-Speech with voice cloning), a hosted MCP server exposing createCall and getCall as native agent tools, an A2A agent card, a published Agent Skill, an llms.txt, webhook push notifications for call completion, and an official Python SDK.

**APIs.json:** [https://sarj-ai-developer-api.apievangelist.com/apis.yml](https://sarj-ai-developer-api.apievangelist.com/apis.yml)

## Tags

- voice AI
- voice agents
- conversational AI
- Arabic AI
- outbound calls
- telephony
- speech to text
- text to speech
- voice cloning
- MCP
- agent-native
- Saudi Arabia
- MENA

## Timestamps

- **Created:** 2026-08-04
- **Modified:** 2026-08-09

## APIs

### Sarj AI Developer API Admin API

The admin API from Sarj AI Developer API — 4 operation(s) for admin.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- admin

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-admin-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-admin-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-admin-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Agent Profiles API

The agent-profiles API from Sarj AI Developer API — 5 operation(s) for agent-profiles.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- agent-profiles

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-agent-profiles-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-agent-profiles-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-agent-profiles-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Analytics API

The analytics API from Sarj AI Developer API — 1 operation(s) for analytics.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- analytics

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-analytics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-analytics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-analytics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Audio API

The Audio API from Sarj AI Developer API — 3 operation(s) for audio.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Audio

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-audio-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-audio-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-audio-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Batch API

The batch API from Sarj AI Developer API — 9 operation(s) for batch.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- batch

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-batch-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-batch-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-batch-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Calls API

Create outbound voice calls and retrieve call details and transcripts.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Calls

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-calls-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-calls-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-calls-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Debug API

The Debug API from Sarj AI Developer API — 1 operation(s) for debug.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Debug

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-debug-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-debug-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-debug-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Health API

The Health API from Sarj AI Developer API — 3 operation(s) for health.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Health

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-health-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-health-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-health-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Integrations API

The integrations API from Sarj AI Developer API — 19 operation(s) for integrations.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- integrations

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-integrations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-integrations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-integrations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Messaging API

The messaging API from Sarj AI Developer API — 8 operation(s) for messaging.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- messaging

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-messaging-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-messaging-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-messaging-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Metrics API

The Metrics API from Sarj AI Developer API — 1 operation(s) for metrics.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Metrics

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-metrics-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-metrics-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-metrics-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Models API

The Models API from Sarj AI Developer API — 2 operation(s) for models.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Models

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-models-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-models-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-models-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Openai API

The Openai API from Sarj AI Developer API — 1 operation(s) for openai.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Openai

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-openai-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-openai-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-openai-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Organization Sip API

The organization-sip API from Sarj AI Developer API — 7 operation(s) for organization-sip.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- organization-sip

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-organization-sip-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-organization-sip-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-organization-sip-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Organization Variables API

The organization-variables API from Sarj AI Developer API — 3 operation(s) for organization-variables.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- organization-variables

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-organization-variables-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-organization-variables-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-organization-variables-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Organizations API

The organizations API from Sarj AI Developer API — 7 operation(s) for organizations.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- organizations

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-organizations-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-organizations-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-organizations-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Report Templates API

The report-templates API from Sarj AI Developer API — 3 operation(s) for report-templates.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- report-templates

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-report-templates-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-report-templates-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-report-templates-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Salesforce API

The salesforce API from Sarj AI Developer API — 2 operation(s) for salesforce.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- salesforce

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-salesforce-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-salesforce-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-salesforce-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Salla API

The salla API from Sarj AI Developer API — 3 operation(s) for salla.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- salla

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-salla-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-salla-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-salla-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Sarj STT API API

The Sarj STT API API from Sarj AI Developer API — 1 operation(s) for sarj stt api.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Sarj STT API

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-sarj-stt-api-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-sarj-stt-api-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-sarj-stt-api-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Settings API

The settings API from Sarj AI Developer API — 7 operation(s) for settings.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- settings

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-settings-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-settings-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-settings-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Sip API

The sip API from Sarj AI Developer API — 7 operation(s) for sip.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- sip

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-sip-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-sip-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-sip-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API System API

Service health and status.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- System

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-system-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-system-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-system-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Task API

The task API from Sarj AI Developer API — 4 operation(s) for task.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- task

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-task-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-task-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-task-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Task Management API

The task-management API from Sarj AI Developer API — 5 operation(s) for task-management.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- task-management

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-task-management-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-task-management-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-task-management-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Voices API

The Voices API from Sarj AI Developer API — 3 operation(s) for voices.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- Voices

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-voices-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-voices-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-voices-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

### Sarj AI Developer API Zoho API

The zoho API from Sarj AI Developer API — 10 operation(s) for zoho.

- **Human URL:** [https://platform-docs.sarj.ai](https://platform-docs.sarj.ai)
- **Base URL:** `https://platform-api.sarj.ai/api/v1`

#### Tags

- zoho

#### Properties

- [OpenAPI](openapi/sarj-ai-developer-api-zoho-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sarj-ai-developer-api-zoho-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sarj-ai-developer-api-zoho-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [M C P](https://platform-api.sarj.ai/api/v1/mcp)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Webhooks](https://platform-docs.sarj.ai/webhooks)
- [Documentation](https://platform-docs.sarj.ai/speech-to-text)
- [Documentation](https://platform-docs.sarj.ai/text-to-speech)

## Common Properties

- [Overlay](overlays/sarj-ai-developer-api-developer-overlay.yaml)
- [Developer Portal](https://platform-docs.sarj.ai)
- [Documentation](https://platform-docs.sarj.ai)
- [API Reference](https://platform-docs.sarj.ai/api-reference)
- [Getting Started](https://platform-docs.sarj.ai/getting-started)
- [Support](mailto:support@sarj.ai)
- [Sign Up](https://platform.sarj.ai/sign-in)
- [GitHub Organization](https://github.com/sarj-ai)
- [L L M S Txt](llms/sarj-ai-developer-api-llms.txt)
- [Agent Card](a2a/sarj-ai-developer-api-a2a.yml)
- [Agent Skill](skills/_index.yml)
- [M C P Server](mcp/sarj-ai-developer-api-mcp.yml)
- [Tool Crosswalk](mcp/sarj-ai-developer-api-tool-crosswalk.yml)
- [Packages](packages/sarj-ai-developer-api-packages.yml)
- [S D Ks](packages/sarj-ai-developer-api-packages.yml)
- [Well Known](well-known/sarj-ai-developer-api-well-known.yml)
- [Authentication](authentication/sarj-ai-developer-api-authentication.yml)
- [O Auth Scopes](scopes/sarj-ai-developer-api-scopes.yml)
- [Domain Security](security/sarj-ai-developer-api-domain-security.yml)
- [Conformance](conformance/sarj-ai-developer-api-conformance.yml)
- [Error Catalog](errors/sarj-ai-developer-api-problem-types.yml)
- [Lifecycle](lifecycle/sarj-ai-developer-api-lifecycle.yml)
- [Conventions](conventions/sarj-ai-developer-api-conventions.yml)
- [Webhooks](asyncapi/sarj-ai-developer-api-webhooks.yml)
- [Data Model](data-model/sarj-ai-developer-api-data-model.yml)
- [Agentic Access](agentic-access/sarj-ai-developer-api-agentic-access.yml)

## Maintainers

**FN:** Sarj AI Developer API
**Email:** contact@sarj.ai
**URL:** https://www.sarj.ai/en/
