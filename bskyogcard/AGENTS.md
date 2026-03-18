# AGENTS.md - OG Card Service (Node/TypeScript Backend)

This file applies to work inside `bskyogcard/`.

## Scope
- Open Graph card rendering service.
- Server-side image generation and OG route handling.

## Validation Checklist
Run from `bskyogcard/`:

1. `yarn build`

## Runtime Smoke Validation
When behavior or route logic changes:

1. Start service: `yarn start`
2. Verify health endpoint: `curl http://localhost:PORT/health`

Use the configured port for your local environment.

## Change-to-Validation Mapping
- Rendering/template/route updates: build + runtime smoke validation.
- Asset/font/script updates: build (and `yarn install-fonts` only if font pipeline changed).
