# AGENTS.md - App Client (React Native + Expo)

This file applies to work inside `src/` and the main app surface (mobile + web client).

## Scope
- Cross-platform app UI, navigation, state, and app business logic.
- Frontend behavior for iOS, Android, and Expo Web.

## Implementation Notes
- Use `#/` import aliases for app code.
- Wrap all user-facing strings for i18n (`msg`, `plural`, `<Trans>`).
- Prefer existing UI primitives from `#/components` and ALF (`#/alf`).
- For dialog follow-ups, use `control.close(() => ...)` to avoid race conditions.
- Do not run `yarn intl:extract` or `yarn intl:compile` manually; CI/nightly handles this.

## Validation Checklist
Run from repo root:

1. `yarn lint`
2. `yarn typecheck`
3. `yarn test`

## Platform-Specific Validation
Use the subset that matches your change:

- Mobile runtime smoke test:
  - `yarn ios` or `yarn android`
- Web client smoke test/build:
  - `yarn web`
  - `yarn build-web`

## Change-to-Validation Mapping
- UI/interaction changes: lint + typecheck + tests + target-platform smoke test.
- Query/state/network logic: lint + typecheck + tests.
- Web-only behavior: lint + typecheck + tests + `yarn build-web`.
