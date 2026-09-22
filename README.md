# DocHub AI

Public AI tooling for building integrations against **DocHub Public API v2** — starting with agent
skills for Cursor, Claude Code, Codex, and others.

Skills do **not** restate auth flows or endpoint parameters. They point at the public developer
portal docs and OpenAPI:

- Docs: https://dev.dochub.com/docs/
- Catalog: https://dev.dochub.com/llms.txt
- OpenAPI: https://dev.dochub.com/api-reference/openapi.yaml

This repository is the **source of truth** for DocHub’s public agent skills (and future AI packs).

## Install agent skills

```bash
npx skills add DocHubInc/dochub-ai
```

Use Node.js 20+. Integrator docs: https://dev.dochub.com/docs/ai-agents

## Skills

| Skill | Use when |
|-------|----------|
| `dochub-best-practices` | Choosing which docs/OpenAPI to open for an integration |
| `dochub-auth` | API key or OAuth setup |
| `dochub-documents` | Documents and document roles |
| `dochub-sign-requests` | Create / list / bulk / resend / void |
| `dochub-webhooks` | Webhook receivers and endpoint management |
| `dochub-docs` | Looking up docs and OpenAPI via `llms.txt` |

## After install

Start a new agent chat, then ask to scaffold an integration (for example OAuth + send a sign request
from a template). Keep credentials in your app’s own env or secret manager.
