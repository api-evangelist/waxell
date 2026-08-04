# Waxell (waxell)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Waxell is an AI agent governance and observability platform that provides runtime policy enforcement, auto-instrumented LLM telemetry, MCP governance, cost management, and durable workflow execution for agents built in any Python framework or third-party agentic tool (Claude Code, Cursor, LangChain, CrewAI, OpenAI Agents SDK, and 200+ more).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/waxell/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/waxell/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- AI Agent Governance
- Observability
- Policy Enforcement
- LLM Telemetry
- Cost Management
- MCP
- Agent Runtime

## Timestamps

- **Created:** 2026-05-06
- **Modified:** 2026-05-19

## APIs

### Waxell Observe API

The Waxell Observe REST API exposes the AI agent governance and observability control plane. It is used by the waxell-observe Python SDK and the Developer MCP server to record runs, log LLM calls, spans, steps and scores, evaluate runtime governance policies, manage prompts, and administer the model cost catalog. Endpoints live under /api/v1/observe/ on a tenant-specific *.waxell.dev host and accept the same wax_sk_ keys via X-Wax-Key or Authorization: Bearer.

- **Human URL:** [https://waxell.ai/docs/observe/api/endpoints](https://waxell.ai/docs/observe/api/endpoints)
- **Base URL:** `https://{tenant}.waxell.dev/api/v1/observe`

#### Tags

- AI Agent Governance
- Observability
- LLM Telemetry
- Policy Enforcement
- Cost Management

#### Properties

- [Documentation](https://waxell.ai/docs)
- [API Reference](https://waxell.ai/docs/observe/api/endpoints)
- [Quickstart](https://waxell.ai/docs/observe/quickstart)
- [Authentication](https://waxell.ai/docs/observe/api/authentication)
- [SDK](https://pypi.org/project/waxell-observe/)
- [OpenAPI](openapi/waxell-observe-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/waxell-observe.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/waxell-observe.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/waxell-run-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/waxell-llm-call-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/waxell-policy-decision-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/waxell-span-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/waxell-run-structure.json)
- [JSON Structure](json-structure/waxell-policy-decision-structure.json)

### Waxell Developer MCP Server

Waxell Developer MCP is a hosted Model Context Protocol server that lets coding agents (Claude Code, Cursor, Windsurf, VS Code, Claude Desktop) query a Waxell instance in real time. It exposes 15 live tools (agent health, error investigation, LLM cost tracking, governance policy review, account signup) plus 8 documentation resources at waxell://docs/*. Connection is SSE; per-client authentication uses Bearer tokens in the Authorization header.

- **Human URL:** [https://waxell.ai/docs/agents/overview](https://waxell.ai/docs/agents/overview)
- **Base URL:** `https://dev-mcp.waxell.dev`

#### Tags

- MCP
- AI Agent Governance
- Developer Tools
- Coding Agents

#### Properties

- [Documentation](https://waxell.ai/docs/agents/overview)
- [API Reference](https://dev-mcp.waxell.dev/sse)
- [Authentication](https://waxell.ai/docs/agents/overview)
- [GitHub Repository](https://gitlab.com/waxell/agentforge)
- [Postman Collection](collections/waxell-observe.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/waxell-observe.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Documentation](https://waxell.ai/docs)
- [Getting Started](https://waxell.ai/docs/observe/quickstart)
- [Quickstart](https://waxell.ai/docs/observe/quickstart)
- [SDK](https://waxell.ai/docs/observe/quickstart)
- [Console](https://waxell.dev)
- [Sign Up](https://waxell.ai/get-access)
- [Pricing](https://waxell.ai/get-access)
- [Plans](plans/waxell-plans-pricing.yml)
- [Rate Limits](rate-limits/waxell-rate-limits.yml)
- [Fin Ops](finops/waxell-finops.yml)
- [Status Page](https://status.waxell.dev)
- [Blog](https://waxell.ai/blog)
- [Glossary](https://waxell.ai/glossary)
- [Security](https://waxell.ai/docs/security)
- [Trust Center](https://app.vanta.com/callsine.com/trust/pg7qc55eh5ge6ejjv7zxksy)
- [Compliance](https://waxell.ai/docs/security)
- [LinkedIn](https://www.linkedin.com/company/waxell-ai)
- [GitHub Repository](https://gitlab.com/waxell/agentforge)
- [Spectral Rules](rules/waxell-rules.yml)
- [Vocabulary](vocabulary/waxell-vocabulary.yml)
- [JSON-LD](json-ld/waxell-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Example](examples/waxell-start-run-example.json)
- [Example](examples/waxell-record-llm-call-example.json)
- [Example](examples/waxell-policy-check-example.json)
- [Example](examples/waxell-get-prompt-example.json)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Solutions](undefined)
- [L L Ms Txt](https://waxell.ai/llms.txt)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
