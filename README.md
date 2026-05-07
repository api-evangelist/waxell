# Waxell (waxell)
Waxell is an AI agent governance and observability platform that provides runtime policy enforcement, auto-instrumented LLM telemetry, MCP governance, cost management, and durable workflow execution for agents built in any Python framework or third-party agentic tool (Claude Code, Cursor, LangChain, CrewAI, OpenAI Agents SDK, and 200+ more).

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/waxell/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - AI Agent Governance, Observability, Policy Enforcement, LLM Telemetry, Cost Management, MCP, Agent Runtime

## Timestamps

- **Created:** 2026-05-06
- **Modified:** 2026-05-06

## APIs

### Waxell Observe API
The Waxell Observe REST API exposes the AI agent governance and observability control plane. It is used by the waxell-observe Python SDK and the Developer MCP server to record runs, log LLM calls, spans, steps and scores, evaluate runtime governance policies, manage prompts, and administer the model cost catalog. Endpoints live under /api/v1/observe/ on a tenant-specific *.waxell.dev host and accept the same wax_sk_ keys via X-Wax-Key or Authorization: Bearer.

**Human URL:** [https://waxell.ai/docs/observe/api/endpoints](https://waxell.ai/docs/observe/api/endpoints)

#### Tags:

 - AI Agent Governance, Observability, LLM Telemetry, Policy Enforcement, Cost Management

#### Properties

- [Documentation](https://waxell.ai/docs)
- [APIReference](https://waxell.ai/docs/observe/api/endpoints)
- [Quickstart](https://waxell.ai/docs/observe/quickstart)
- [Authentication](https://waxell.ai/docs/observe/api/authentication)
- [SDK](https://pypi.org/project/waxell-observe/)
- [OpenAPI](openapi/waxell-observe-openapi.yml)
- [JSONSchema](json-schema/waxell-run-schema.json)
- [JSONSchema](json-schema/waxell-llm-call-schema.json)
- [JSONSchema](json-schema/waxell-policy-decision-schema.json)
- [JSONSchema](json-schema/waxell-span-schema.json)
- [JSONStructure](json-structure/waxell-run-structure.json)
- [JSONStructure](json-structure/waxell-policy-decision-structure.json)

### Waxell Developer MCP Server
Waxell Developer MCP is a hosted Model Context Protocol server that lets coding agents (Claude Code, Cursor, Windsurf, VS Code, Claude Desktop) query a Waxell instance in real time. It exposes 15 live tools (agent health, error investigation, LLM cost tracking, governance policy review, account signup) plus 8 documentation resources at waxell://docs/*. Connection is SSE; per-client authentication uses Bearer tokens in the Authorization header.

**Human URL:** [https://waxell.ai/docs/agents/overview](https://waxell.ai/docs/agents/overview)

#### Tags:

 - MCP, AI Agent Governance, Developer Tools, Coding Agents

#### Properties

- [Documentation](https://waxell.ai/docs/agents/overview)
- [APIReference](https://dev-mcp.waxell.dev/sse)
- [Authentication](https://waxell.ai/docs/agents/overview)
- [GitHubRepository](https://gitlab.com/waxell/agentforge)

## Common Properties

- [Documentation](https://waxell.ai/docs)
- [GettingStarted](https://waxell.ai/docs/observe/quickstart)
- [Quickstart](https://waxell.ai/docs/observe/quickstart)
- [SDK](https://waxell.ai/docs/observe/quickstart)
- [Console](https://waxell.dev)
- [SignUp](https://waxell.ai/get-access)
- [Pricing](https://waxell.ai/get-access)
- [Plans](plans/waxell-plans-pricing.yml)
- [RateLimits](rate-limits/waxell-rate-limits.yml)
- [FinOps](finops/waxell-finops.yml)
- [StatusPage](https://status.waxell.dev)
- [Blog](https://waxell.ai/blog)
- [Glossary](https://waxell.ai/glossary)
- [Security](https://waxell.ai/docs/security)
- [TrustCenter](https://app.vanta.com/callsine.com/trust/pg7qc55eh5ge6ejjv7zxksy)
- [Compliance](https://waxell.ai/docs/security)
- [LinkedIn](https://www.linkedin.com/company/waxell-ai)
- [GitHubRepository](https://gitlab.com/waxell/agentforge)
- [SpectralRules](rules/waxell-rules.yml)
- [Vocabulary](vocabulary/waxell-vocabulary.yml)
- [NaftikoCapability](capabilities/agent-governance.yaml)
- [NaftikoCapability](capabilities/shared/observe.yaml)
- [JSON-LD](json-ld/waxell-context.jsonld)
- [Example](examples/waxell-start-run-example.json)
- [Example](examples/waxell-record-llm-call-example.json)
- [Example](examples/waxell-policy-check-example.json)
- [Example](examples/waxell-get-prompt-example.json)

## Features

| Name | Description |
|------|-------------|
| Auto-Instrumentation | Two-line setup auto-instruments 200+ libraries (OpenAI, Anthropic, LangChain, LlamaIndex, CrewAI, LiteLLM, etc.) without code changes. |
| Runtime Policy Enforcement | 26 policy categories (cost, kill switch, PII, compliance, scope, safety) returning seven decisions (allow, warn, redact, throttle, block, skip, retry). |
| MCP Governance | Auto-instrumentor, server middleware, and governance proxy for Model Context Protocol traffic with PII scanning and rug-pull detection. |
| Cost Management | Built-in model pricing for 20+ models, tenant overrides via REST, budget enforcement that warns/throttles/blocks at thresholds. |
| Prompt Management | Versioned managed prompts retrievable by name and label (e.g. production, staging) directly from the SDK. |
| Workflow Envelope | Durable execution boundary with checkpoint and resume; Redis-backed in production, in-memory for development. |
| Human-in-the-Loop Approvals | Custom handlers route policy blocks to Slack, webhooks, or terminal prompts for human review. |
| Audit Trail | Immutable, timestamped record of all agent actions, decisions, and governance events. |
| Developer MCP | Hosted SSE MCP server (dev-mcp.waxell.dev/sse) with 15 live tools and 8 docs resources for coding agents. |
| Field-Level Encryption | PII fields encrypted at the application layer with AES-256-GCM and AWS KMS (FIPS 140-2 Level 3) before database storage. |

## Use Cases

| Name | Description |
|------|-------------|
| Govern Third-Party Coding Agents | Enforce policies on Claude Code, Cursor, Windsurf, VS Code, and Claude Desktop without modifying their code. |
| Instrument Self-Built Agents | Add full observability to LangChain, CrewAI, OpenAI Agents SDK, or custom Python agents with the @waxell.observe decorator. |
| Cost-Capped Agent Deployment | Set budgets on token spend per agent, user, or tenant; block runs that exceed configured limits. |
| PII-Safe MCP Tool Use | Scan MCP tool inputs/outputs for PII, credentials, and secrets with warn/block/redact responses. |
| Durable Long-Running Workflows | Use the WorkflowEnvelope to checkpoint multi-step agent workflows so they can resume after interruption. |
| Compliance-Ready AI Operations | Maintain SOC 2 Ready posture with immutable audit trails, encrypted PII, and EU data residency. |

## Integrations

| Name | Description |
|------|-------------|
| OpenAI | Auto-instrumented LLM provider; cost and token tracking out of the box. |
| Anthropic | Auto-instrumented LLM provider; supports Claude family models. |
| LangChain / LangGraph | First-class callback handler (WaxellLangChainHandler) for tracing chains and graphs. |
| CrewAI | Auto-instrumented multi-agent framework support. |
| LlamaIndex | Tracing for RAG pipelines built with LlamaIndex. |
| LiteLLM | Unified telemetry across LiteLLM-routed providers. |
| Claude Code | Governance overlay for Anthropic's Claude Code coding agent via the Developer MCP. |
| Cursor / Windsurf / VS Code | Coding-agent governance via the SSE MCP server at dev-mcp.waxell.dev. |
| OpenAI Agents SDK | Auto-instrumentation for OpenAI's Agents SDK runs. |
| AWS Bedrock / Azure OpenAI / Google Vertex AI | Cloud LLM providers covered by Waxell's auto-instrumentation. |
| Pinecone / Weaviate / Qdrant / Milvus / Chroma | Vector database call tracing with retrieval span recording. |
| Slack / Webhooks | Human-in-the-loop approval handlers for policy blocks. |
| Stripe | Listed subprocessor for billing. |

## Solutions

| Name | Description |
|------|-------------|
| Connect | Govern third-party agents (Claude Code, Cursor) without code changes via the MCP governance proxy. |
| Observe | Instrument self-built agents with auto-instrumentation, policy enforcement, and cost attribution. |
| Runtime | Governed execution environment for high-risk workflows with the durable WorkflowEnvelope. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Waxell Observe API](openapi/waxell-observe-openapi.yml)

### JSON Schema

- [Waxell Run Schema](json-schema/waxell-run-schema.json)
- [Waxell LLM Call Schema](json-schema/waxell-llm-call-schema.json)
- [Waxell Policy Decision Schema](json-schema/waxell-policy-decision-schema.json)
- [Waxell Span Schema](json-schema/waxell-span-schema.json)

### JSON Structure

- [Waxell Run Structure](json-structure/waxell-run-structure.json)
- [Waxell Policy Decision Structure](json-structure/waxell-policy-decision-structure.json)

### JSON-LD

- [Waxell Context](json-ld/waxell-context.jsonld)

### Examples

- [Start Run Example](examples/waxell-start-run-example.json)
- [Record LLM Call Example](examples/waxell-record-llm-call-example.json)
- [Policy Check Example](examples/waxell-policy-check-example.json)
- [Get Prompt Example](examples/waxell-get-prompt-example.json)

### Plans, Rate Limits, FinOps

- [Plans & Pricing](plans/waxell-plans-pricing.yml)
- [Rate Limits](rate-limits/waxell-rate-limits.yml)
- [FinOps](finops/waxell-finops.yml)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Waxell Observe](capabilities/shared/observe.yaml) — 11 operations covering runs, telemetry, prompts, governance, and model costs

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Agent Governance](capabilities/agent-governance.yaml) | waxell-observe | 8 | Platform Engineer / Agent Developer / FinOps Analyst |

## Vocabulary

- [Waxell Vocabulary](vocabulary/waxell-vocabulary.yml) — Unified taxonomy mapping 9 resources, 8 actions, 1 workflow, and 3 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Waxell Spectral Rules](rules/waxell-rules.yml) — 14 rules enforcing Waxell title, server, path, operation, schema, and security conventions

## Maintainers

**FN:** Kin Lane

**Email:** info@apievangelist.com
