# Verification

Verify only dimensions relevant to the requested clone, but never skip basic launch and boundary checks.

## Baseline

- Start the local result from a clean command or documented entry point.
- Confirm there are no broken local paths, missing primary assets, or accidental live mutations.
- Confirm secrets, cookies, tokens, personal data, and production endpoints are absent from deliverables.

## Website and frontend

- Compare source and local result at the same viewport.
- Check desktop and mobile by default; add tablet only when requested or layout behavior differs.
- Check typography, spacing, colors, major component geometry, navigation, hover/focus states, and the requested flows.
- Use `decant verify` for a mirrored capture when available; inspect its live/local screenshots and repair hints instead of relying only on a score.
- Record inaccessible pages, blocked assets, dynamic data, and server-dependent states.

## App reconstruction

- Map each requested feature to evidence and an implementation status.
- Test the rebuilt flow with local or mock data.
- Distinguish visual parity, interaction parity, and business-rule parity.
- Treat authentication, payments, licensing, push notifications, sync, device services, and remote APIs as separate integrations unless directly implemented and verified.

## Claim language

Use:

- `Verified`: directly compared or tested.
- `Observed`: present in the supplied target or capture.
- `Inferred`: likely from evidence but not directly observed.
- `Mocked`: intentionally local or simulated.
- `Unknown`: not accessible within the inspection boundary.

Never upgrade an `inferred`, `mocked`, or `unknown` item to `verified` for presentation convenience.
