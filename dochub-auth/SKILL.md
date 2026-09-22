---
name: dochub-auth
description: >-
  Use when implementing DocHub Public API authentication (API keys or OAuth 2.0).
  Points to portal auth docs and OpenAPI — do not invent flows from memory.
---

# Authentication

Implement auth using the **developer portal documentation** and OpenAPI. Do not restate grant types, headers, or token fields here — read the sources below.

## Documentation

- https://dev.dochub.com/docs/authentication.md
- https://dev.dochub.com/docs/authentication/api-key.md
- https://dev.dochub.com/docs/authentication/oauth.md

## OpenAPI

- https://dev.dochub.com/api-reference/tag/oauth.yaml
- https://dev.dochub.com/api-reference/tag/oauth-applications.yaml
- Catalog of every tag: https://dev.dochub.com/llms.txt

## Agent behavior

1. Read the auth docs that match the product model (API key vs OAuth).
2. Confirm request/response shapes from the tag YAML above.
3. Wire credentials into the user’s app using their existing secret/env conventions.
