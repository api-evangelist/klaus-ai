# Klaus AI

Klaus is a managed cloud hosting platform for OpenClaw AI agents, built by **Usebits Inc** (Y Combinator W26, San Francisco), founded by Bailey Wickham and Robbie Thompson. Klaus provisions an isolated, pre-configured OpenClaw instance on dedicated AWS ARM compute in about five minutes, with messaging channels (Slack, Telegram, WhatsApp, iMessage, Discord), Google Workspace, browser automation, AgentMail email, GitHub backup, Tailscale SSH, scheduled cron tasks, semantic memory, and inbound instance webhooks.

- Website: https://klausai.com/
- FAQ (closest thing to developer docs): https://klausai.com/faq/
- Blog: https://klausai.com/blog/
- Pricing: https://klausai.com/klaus/subscribe

## API surface

Klaus publishes **no OpenAPI description**. The platform API at `https://api.klausai.com` is a tRPC surface, plus an OpenAI-compatible `POST /openclaw/v1/chat/completions` proxy. Everything catalogued in this repo about that surface was read from the provider's own published npm client, [`@klausai/cli`](https://www.npmjs.com/package/@klausai/cli) — no shapes were invented.

Auth is an API key in the `x-api-key` header (created at https://klausai.com/account) or a bearer session token from an OAuth 2.0 Device Authorization Grant (RFC 8628).

## Artifacts

| Artifact | File |
|---|---|
| Packages / SDKs | `packages/klaus-ai-packages.yml` |
| CLI | `cli/klaus-ai-cli.yml` |
| Authentication | `authentication/klaus-ai-authentication.yml` |
| Conventions | `conventions/klaus-ai-conventions.yml` |
| Error catalog | `errors/klaus-ai-problem-types.yml` |
| Webhooks | `asyncapi/klaus-ai-webhooks.yml` |
| MCP (candidate only — Klaus runs no MCP server) | `mcp/klaus-ai-mcp.yml` |
| Conformance | `conformance/klaus-ai-conformance.yml` |
| Lifecycle | `lifecycle/klaus-ai-lifecycle.yml` |
| Well-known probe | `well-known/klaus-ai-well-known.yml` |
| Domain security | `security/klaus-ai-domain-security.yml` |
| llms.txt | `llms/klaus-ai-llms.txt` |

## Recorded absences (as of 2026-07-19)

No OpenAPI, no AsyncAPI, no status page, no changelog, no deprecation policy, no `/.well-known/` documents, no `llms.txt`, no vulnerability-disclosure program, no trust center, and no published compliance certifications. `klausai.com` and `app.usebits.com` return HTTP 200 with the SPA shell for any unknown path, so discovery probes were verified by body comparison rather than status code.

Backed by: y-combinator
