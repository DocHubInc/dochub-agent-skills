---
name: dochub-sign-requests
description: >-
  Use when building or debugging sign-request flows. Read the portal OpenAPI and
  API reference; do not restate request parameters from memory.
---

# Sign requests

Build create / list / bulk / resend / void flows from the **published OpenAPI** on the developer portal. Do not copy parameter lists into the user’s code from memory — fetch the YAML and follow it.

## OpenAPI

- https://dev.dochub.com/api-reference/tag/sign-requests.yaml
- Catalog of every tag: https://dev.dochub.com/llms.txt

## Auth docs (sign-request calls need the right scheme)

- https://dev.dochub.com/docs/authentication.md
- https://dev.dochub.com/docs/authentication/oauth.md

## Agent behavior

1. Fetch the Sign Requests tag YAML and locate operations before writing client code.
2. Prefer current operations described there; treat any marked deprecated as fallback only.
3. Recommend webhooks for reliable status: see `dochub-webhooks`.
