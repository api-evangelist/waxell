# Waxell (waxell)

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
