# Sarj AI Developer API

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

Sarj.ai is a voice and chat AI agent platform built for Arabic, English and Urdu, focused on the Saudi and wider MENA market. The public developer surface is a REST API for outbound voice calls — place a call against a saved scenario (immediately, or booked up to 30 days ahead), cancel or reschedule it while it is still pending, create a retry policy governing how often a number is re-dialed, and retrieve the call's status, recording, transcript and asynchronous post-call outcome report. Alongside the call API, Sarj publishes two OpenAI-compatible speech APIs (Speech-to-Text with streaming, and Text-to-Speech with voice cloning), a hosted MCP server exposing createCall and getCall as native agent tools, a second unauthenticated MCP server over its documentation, an A2A agent card, a published Agent Skill with an agentskills.io discovery index, an llms.txt, webhook push notifications covering eleven call outcomes, and an official Python SDK.

**Areas:** Voice AI · Voice Agents · Conversational AI · Arabic AI · Outbound Calls · Telephony · Speech-to-Text · Text-to-Speech · Voice Cloning · MCP · Agent-Native · Saudi Arabia

## Sarj AI Developer API on APIs.io

Everything profiled for Sarj AI Developer API is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/sarj-ai-developer-api/](https://apis.io/providers/sarj-ai-developer-api/)** — or go straight to one of the APIs or properties below.

### APIs (49)

- [Sarj AI Developer API Agent Profiles API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-agent-profiles-api/) — The agent-profiles API from Sarj AI Developer API — 5 operation(s) for agent-profiles.
- [Sarj AI Developer API Analytics API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-analytics-api/) — The analytics API from Sarj AI Developer API — 1 operation(s) for analytics.
- [Sarj AI Developer API Audio API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-audio-api/) — The Audio API from Sarj AI Developer API — 3 operation(s) for audio.
- [Sarj AI Developer API Batch API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-batch-api/) — The batch API from Sarj AI Developer API — 9 operation(s) for batch.
- [Sarj AI Developer API Calls API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-calls-api/) — Create outbound voice calls and retrieve call details and transcripts.
- [Sarj AI Developer API Debug API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-debug-api/) — The Debug API from Sarj AI Developer API — 1 operation(s) for debug.
- [Sarj AI Developer API Health API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-health-api/) — The Health API from Sarj AI Developer API — 3 operation(s) for health.
- [Sarj AI Developer API Integrations API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-integrations-api/) — The integrations API from Sarj AI Developer API — 19 operation(s) for integrations.
- [Sarj AI Developer API Messaging API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-messaging-api/) — The messaging API from Sarj AI Developer API — 8 operation(s) for messaging.
- [Sarj AI Developer API Metrics API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-metrics-api/) — The Metrics API from Sarj AI Developer API — 1 operation(s) for metrics.
- [Sarj AI Developer API Models API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-models-api/) — The Models API from Sarj AI Developer API — 2 operation(s) for models.
- [Sarj AI Developer API Openai API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-openai-api/) — The Openai API from Sarj AI Developer API — 1 operation(s) for openai.
- [Sarj AI Developer API Organization Sip API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-organization-sip-api/) — The organization-sip API from Sarj AI Developer API — 7 operation(s) for organization-sip.
- [Sarj AI Developer API Organization Variables API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-organization-variables-api/) — The organization-variables API from Sarj AI Developer API — 3 operation(s) for organization-variables.
- [Sarj AI Developer API Organizations API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-organizations-api/) — The organizations API from Sarj AI Developer API — 7 operation(s) for organizations.
- [Sarj AI Developer API Report Templates API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-report-templates-api/) — The report-templates API from Sarj AI Developer API — 3 operation(s) for report-templates.
- [Sarj AI Developer API Sarj STT API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-sarj-stt-api-api/) — The Sarj STT API API from Sarj AI Developer API — 1 operation(s) for sarj stt api.
- [Sarj AI Developer API Settings API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-settings-api/) — The settings API from Sarj AI Developer API — 7 operation(s) for settings.
- [Sarj AI Developer API Sip API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-sip-api/) — The sip API from Sarj AI Developer API — 7 operation(s) for sip.
- [Sarj AI Developer API System API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-system-api/) — Service health and status.
- [Sarj AI Developer API Task API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-task-api/) — The task API from Sarj AI Developer API — 4 operation(s) for task.
- [Sarj AI Developer API Task Management API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-task-management-api/) — The task-management API from Sarj AI Developer API — 5 operation(s) for task-management.
- [Sarj AI Developer API Voices API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-voices-api/) — The Voices API from Sarj AI Developer API — 3 operation(s) for voices.
- [Sarj AI Developer API API Keys API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-api-keys-api/) — The api-keys API from Sarj AI Developer API — 3 operation(s) for api-keys.
- [Sarj AI Developer API Call Flags API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-call-flags-api/) — The call-flags API from Sarj AI Developer API — 4 operation(s) for call-flags.
- [Sarj AI Developer API Custom Scenarios API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-custom-scenarios-api/) — The custom-scenarios API from Sarj AI Developer API — 5 operation(s) for custom-scenarios.
- [Sarj AI Developer API Kamailio State API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-kamailio-state-api/) — The kamailio-state API from Sarj AI Developer API — 1 operation(s) for kamailio-state.
- [Sarj AI Developer API Knowledge Bases API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-knowledge-bases-api/) — The knowledge-bases API from Sarj AI Developer API — 7 operation(s) for knowledge-bases.
- [Sarj AI Developer API Livez API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-livez-api/) — The Livez API from Sarj AI Developer API — 1 operation(s) for livez.
- [Sarj AI Developer API Messaging Settings API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-messaging-settings-api/) — The messaging-settings API from Sarj AI Developer API — 4 operation(s) for messaging-settings.
- [Sarj AI Developer API Organization Batch Settings API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-organization-batch-settings-api/) — The organization-batch-settings API from Sarj AI Developer API — 1 operation(s) for organization-batch-settings.
- [Sarj AI Developer API Organization Settings API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-organization-settings-api/) — The organization-settings API from Sarj AI Developer API — 1 operation(s) for organization-settings.
- [Sarj AI Developer API Phone Numbers API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-phone-numbers-api/) — The phone-numbers API from Sarj AI Developer API — 13 operation(s) for phone-numbers.
- [Sarj AI Developer API Phone Provider API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-phone-provider-api/) — The phone-provider API from Sarj AI Developer API — 2 operation(s) for phone-provider.
- [Sarj AI Developer API Readyz API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-readyz-api/) — The Readyz API from Sarj AI Developer API — 1 operation(s) for readyz.
- [Sarj AI Developer API Reports API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-reports-api/) — The reports API from Sarj AI Developer API — 2 operation(s) for reports.
- [Sarj AI Developer API Salesforce Integration API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-salesforce-integration-api/) — The salesforce-integration API from Sarj AI Developer API — 2 operation(s) for salesforce-integration.
- [Sarj AI Developer API Salla Integration API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-salla-integration-api/) — The salla-integration API from Sarj AI Developer API — 7 operation(s) for salla-integration.
- [Sarj AI Developer API Scenario Generation API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-scenario-generation-api/) — The scenario-generation API from Sarj AI Developer API — 5 operation(s) for scenario-generation.
- [Sarj AI Developer API Scenario Insights API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-scenario-insights-api/) — The scenario-insights API from Sarj AI Developer API — 2 operation(s) for scenario-insights.
- [Sarj AI Developer API Scenario Templates API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-scenario-templates-api/) — The scenario-templates API from Sarj AI Developer API — 6 operation(s) for scenario-templates.
- [Sarj AI Developer API Schedule Configs API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-schedule-configs-api/) — Create and manage retry policies for scheduled outbound calls.
- [Sarj AI Developer API Sip Connection API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-sip-connection-api/) — The sip-connection API from Sarj AI Developer API — 4 operation(s) for sip-connection.
- [Sarj AI Developer API Sip Connections API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-sip-connections-api/) — The sip-connections API from Sarj AI Developer API — 6 operation(s) for sip-connections.
- [Sarj AI Developer API Sip Provisioning API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-sip-provisioning-api/) — The sip-provisioning API from Sarj AI Developer API — 3 operation(s) for sip-provisioning.
- [Sarj AI Developer API Sip Trunk API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-sip-trunk-api/) — The sip_trunk API from Sarj AI Developer API — 2 operation(s) for sip_trunk.
- [Sarj AI Developer API Users API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-users-api/) — The users API from Sarj AI Developer API — 8 operation(s) for users.
- [Sarj AI Developer API Webhooks API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-webhooks-api/) — The webhooks API from Sarj AI Developer API — 3 operation(s) for webhooks.
- [Sarj AI Developer API Zoho Integration API](https://apis.io/apis/sarj-ai-developer-api/sarj-ai-developer-api-zoho-integration-api/) — The zoho-integration API from Sarj AI Developer API — 12 operation(s) for zoho-integration.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Sarj Ai Developer Api Webhooks](https://apis.io/asyncapis/sarj-ai-developer-api/sarj-ai-developer-api-webhooks/)

#### MCP servers (2)

Model Context Protocol servers that expose the API to agents.

- [mcp](https://apis.io/servers/sarj-ai-developer-api/mcp/)
- [Moved to /providers/sarj-ai-developer-api/](https://apis.io/servers/sarj-ai-developer-api/sarj-voice/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Sarj Ai Developer Api Agentic Access](https://apis.io/agentic-access/sarj-ai-developer-api/sarj-ai-developer-api-agentic-access/)

#### Collections (31)

Postman and Open Collection request collections.

- [Sarj.ai Voice Admin API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-admin-api/)
- [Sarj.ai Voice Agent Profiles API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-agent-profiles-api/)
- [Sarj.ai Voice Analytics API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-analytics-api/)
- [Sarj TTS Audio API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-audio-api/)
- [Sarj.ai Voice Batch API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-batch-api/)
- [Sarj Ai Developer Calls API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-calls-api/)
- [Sarj STT Debug API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-debug-api/)
- [Sarj.ai Developer API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-developer/)
- [Sarj Ai Developer Health API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-health-api/)
- [Sarj.ai Voice Integrations API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-integrations-api/)
- [Sarj.ai Voice Messaging API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-messaging-api/)
- [Sarj TTS Metrics API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-metrics-api/)
- [Sarj TTS Models API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-models-api/)
- [Sarj STT Openai API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-openai-api/)
- [Sarj.ai Voice Organization Sip API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-organization-sip-api/)
- [Sarj.ai Voice Organization Variables API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-organization-variables-api/)
- [Sarj.ai Voice Organizations API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-organizations-api/)
- [Sarj.ai Voice Report Templates API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-report-templates-api/)
- [Sarj.ai Voice Salesforce API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-salesforce-api/)
- [Sarj.ai Voice Salla API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-salla-api/)
- [Sarj STT Sarj STT API API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-sarj-stt-api-api/)
- [Sarj.ai Voice Settings API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-settings-api/)
- [Sarj.ai Voice Sip API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-sip-api/)
- [Sarj STT API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-stt/)
- [Sarj.ai Developer System API](https://apis.io/collections/sarj-ai-developer-api/open-sarj-ai-developer-api-system-api/)
- …and 6 more published on APIs.io

#### Overlays (3)

OpenAPI overlays, including conversational phrasing for each operation.

- [Sarj Ai Developer Api Developer Overlay](https://apis.io/overlays/sarj-ai-developer-api/sarj-ai-developer-api-developer-overlay/)
- [Sarj Ai Developer Api Stt Overlay](https://apis.io/overlays/sarj-ai-developer-api/sarj-ai-developer-api-stt-overlay/)
- [Sarj Ai Developer Api Tts Overlay](https://apis.io/overlays/sarj-ai-developer-api/sarj-ai-developer-api-tts-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Sarj Ai Developer Api Authentication](https://apis.io/security/sarj-ai-developer-api/sarj-ai-developer-api-authentication/)
- [Sarj Ai Developer Api Domain Security](https://apis.io/security/sarj-ai-developer-api/sarj-ai-developer-api-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Sarj Ai Developer Api Scopes](https://apis.io/scopes/sarj-ai-developer-api/sarj-ai-developer-api-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Sarj Ai Developer Api Plans Pricing](https://apis.io/plans/sarj-ai-developer-api/sarj-ai-developer-api-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Sarj Ai Developer Api Rate Limits](https://apis.io/rate-limits/sarj-ai-developer-api/sarj-ai-developer-api-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.sarj.ai/)
- [Documentation](https://platform-docs.sarj.ai)
- [Getting started](https://platform-docs.sarj.ai/getting-started)
- [API reference](https://platform-docs.sarj.ai/api-reference)
- [Sign up](https://platform.sarj.ai/sign-in)
- [Blog](https://blog.sarj.ai)
- [Terms of service](https://sarj.ai/terms)
- [Privacy policy](https://sarj.ai/privacy)
- [GitHub](https://github.com/sarj-ai)

## API Evangelist rating

**Kin Score 41.2** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 48.7 |
| Contract governance | 18.2 |
| Operational transparency | 2.6 |
| Developer ergonomics | 33.3 |
| Access clarity | 21.1 |

**Agent readiness 65.6** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | yes |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | conformant |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 33.0** — AI & Biometrics

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/sarj-ai-developer-api/](https://apis.io/providers/sarj-ai-developer-api/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Sarj AI Developer API: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/sarj-ai-developer-api/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
