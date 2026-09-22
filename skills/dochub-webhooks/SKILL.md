---
name: dochub-webhooks
description: >-
  Use when adding webhook receivers or managing webhook endpoints. Read portal
  webhook docs and OpenAPI.
---

# Webhooks

Use portal **webhook documentation** for setup, verification, deliveries, and events. Use published OpenAPI for HTTP API shapes. Do not restate headers, payload fields, or event catalogs here.

## Documentation

- https://dev.dochub.com/docs/webhooks.md
- https://dev.dochub.com/docs/webhooks/configuration.md
- https://dev.dochub.com/docs/webhooks/receiving.md
- https://dev.dochub.com/docs/webhooks/deliveries.md
- https://dev.dochub.com/docs/webhooks/events.md

## OpenAPI

- https://dev.dochub.com/api-reference/tag/webhooks.yaml
- Catalog of every tag: https://dev.dochub.com/llms.txt

## Agent behavior

1. Read receiving + events docs before writing a receiver.
2. Confirm manage-endpoint operations from the Webhooks tag YAML when coding against the API.
