# DocHub agent skills

Thin agent skills that help coding agents (Cursor, Claude Code, Codex, and others) build integrations against **DocHub Public API v2**.

Skills do **not** restate auth flows or endpoint parameters. They point at the public developer portal docs and OpenAPI:

- Docs: https://dev.dochub.com/docs/
- Catalog: https://dev.dochub.com/llms.txt
- OpenAPI: https://dev.dochub.com/api-reference/openapi.yaml

This repository is the **source of truth**. A GitHub Action syncs `dochub-*/` and `index.json` into [`dochub-developer-portal`](https://github.com/DocHubInc/dochub-developer-portal) at `public/.well-known/skills/` so portal-hosted install stays in sync.

## Install

```bash
npx skills add DocHubInc/dochub-agent-skills
```

Or from the developer portal (after sync has landed):

```bash
npx skills add https://dev.dochub.com
```

Use Node.js 20+.

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

Start a new agent chat, then ask to scaffold an integration (for example OAuth + send a sign request from a template). Keep credentials in your app’s own env or secret manager.

## Sync to developer portal

Workflow: [`.github/workflows/sync-developer-portal.yml`](.github/workflows/sync-developer-portal.yml)

On every push to `main` that touches skills (or via **Actions → Sync: Developer portal skills → Run workflow**), CI:

1. Copies this repo’s skills into `DocHubInc/dochub-developer-portal` → `public/.well-known/skills/`
2. Opens a PR on the portal (`chore/agent-skills-sync`)
3. Tries to enable auto-merge (optional; needs the sync App on the portal’s bypass list)
