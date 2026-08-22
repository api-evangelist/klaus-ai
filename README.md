# Klaus AI

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
