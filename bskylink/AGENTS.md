# AGENTS.md - bskylink Service (Node/TypeScript Backend)

This file applies to work inside `bskylink/`.

## Scope
- Link routing/redirect backend service.
- DB-backed logic, safety-link behavior, and HTTP route handling.

## Validation Checklist
Run from `bskylink/`:

1. `yarn build`
2. `yarn test`

## Notes
- `yarn test` uses `./tests/infra/with-test-db.sh` and expects test DB infra.
- If tests cannot start because infra is unavailable, at minimum run `yarn build` and document the test blocker.

## Change-to-Validation Mapping
- Route/controller or redirect logic: build + test.
- DB schema/migration/data-access changes: build + test.
- Config/bootstrap/logging-only changes: build (and test when feasible).
