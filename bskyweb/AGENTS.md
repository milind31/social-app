# AGENTS.md - bskyweb (Go Web/App Server)

This file applies to work inside `bskyweb/`.

## Scope
- Go-based web server binaries (`bskyweb`, `embedr`).
- HTML templates/static serving and server-side route/filter logic.

## Validation Checklist
Run from `bskyweb/`:

1. `make lint`
2. `make test`
3. `make build`

## Additional Validation
Use when relevant:

- Compile-only check: `make check`
- Formatting fixes: `make fmt`
- Local runtime smoke test:
  - `make run-dev-bskyweb`
  - `make run-dev-embedr`

## Change-to-Validation Mapping
- Go logic changes: lint + test + build.
- Template/static wiring changes: lint + test + build + local runtime smoke check.
- Dependency/config changes: lint + test + build.
