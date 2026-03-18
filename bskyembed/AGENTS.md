# AGENTS.md - Embed Frontend (Preact + Vite)

This file applies to work inside `bskyembed/`.

## Scope
- Embed widget frontend built with Preact/Vite.
- Browser behavior for embeddable post UI and snippet output.

## Validation Checklist
Run from `bskyembed/`:

1. `yarn lint`
2. `yarn typecheck`
3. `yarn build`

## Additional Validation
Run these when relevant:

- Snippet output changed: `yarn build-snippet`
- Local browser sanity check: `yarn dev`

## Change-to-Validation Mapping
- TS/logic changes: lint + typecheck + build.
- CSS/layout/embed rendering changes: lint + typecheck + build + local `yarn dev` check.
- Snippet pipeline changes: lint + typecheck + `yarn build` + `yarn build-snippet`.
