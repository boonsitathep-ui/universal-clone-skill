---
name: universal-clone
description: Clone or reconstruct websites, web apps, desktop apps, Electron packages, APKs, and screenshot-based interfaces. Use when the user wants a local mirror, faithful frontend, functional prototype, clean-room reconstruction, design extraction, or evidence-based comparison of an existing digital product.
---

# Universal Clone

Turn an authorized target into the closest useful local result while preserving a clear boundary between captured assets, observed behavior, inferred behavior, and newly implemented behavior.

## Start with the outcome

Identify the target from the conversation or attached/open material. If a missing choice would materially change the work, ask one compact question containing only the relevant choices:

- **Mirror:** offline/local copy of pages and public assets.
- **Visual clone:** responsive UI with the same appearance and interaction feel.
- **Functional prototype:** frontend flows backed by mock or local data.
- **Reconstruction:** investigate a shipped app and rebuild selected behavior.
- **Migration:** reproduce an owned product from its source repository and data contracts.

Also resolve scope only when missing: one screen/page, selected flow, or whole accessible product. Ask no more than three short questions at once. Do not re-ask facts already supplied. Begin read-only inspection immediately when target and outcome are clear.

## Route by evidence, not ambition

Read [references/routing.md](references/routing.md) after identifying the target type. Prefer the lowest-cost route that can meet the requested fidelity.

- Public/static website or SPA capture: use `decant` first.
- Existing source repository: inspect and implement with normal repository tools.
- User-owned browser page, Electron app, APK, native binary, or packaged app: use `reverse-engineer-anything` and its available REA tools.
- Screenshot, mockup, or image-only target: rebuild from visual evidence; verify against the image.
- Design language only: use `design-mirror` only when its Bright Data requirements are already available or the user chooses that dependency.
- Live interactive frontend clone in a supported Product Design environment: use `url-to-code` when available.

Do not run several capture systems by default. Escalate only when the first route leaves a specific evidence gap.

## Economical default

For websites, start with a single-page static `decant` capture. Inspect `context.md`, `manifest.json`, `design-tokens.json`, and `repair-hints.json` before reading large HTML, CSS, or bundles. Add browser rendering, screenshots, runtime capture, or crawl depth only when needed. Use low concurrency and a polite rate limit for multi-page work.

For apps, start with inventory and summary evidence. Trace only the requested screens or features. Reuse retained evidence and existing sessions rather than repeating analysis.

## Authorization and fidelity boundaries

Proceed only with public material or targets the user is authorized to inspect and reproduce. Never bypass authentication, paywalls, DRM, license checks, access controls, anti-bot protections, or rate limits. Do not extract credentials, tokens, personal data, private API responses, or protected media into the deliverable.

Authentication material may be used only when the user explicitly supplies or authorizes it for their own target. Keep it out of source files, logs, screenshots, reports, and final output. Pause before using cookies or credentials if that authorization is not explicit.

Do not present copied trademarks, proprietary copy, customer data, or third-party assets as the user's original work. For external/public deliverables, replace brand identifiers and restricted content unless the user owns them or explicitly requests an authorized internal replica.

A client cannot reveal an unseen backend. Never claim that a website or binary capture cloned its server, database, private APIs, admin rules, or production data. Implement those parts separately with mock/local data or documented integrations, and label them as new implementation.

## Build contract

1. Record the target, requested outcome, scope, platform, and evidence boundary.
2. Capture the smallest useful evidence set. Preserve source URLs, artifact identity, viewport, and capture date.
3. Produce a route/screen inventory and mark each item `observed`, `inferred`, `new`, or `unknown`.
4. Build into a new local output directory. Never overwrite the source target or modify production.
5. Keep network calls disabled or mocked unless the user explicitly asks for an integration.
6. Verify proportionally to the request using [references/verification.md](references/verification.md).
7. Report what is faithful, approximated, mocked, missing, and unverified.

Pause for approval before publishing, deploying, sending data, using production credentials, calling mutation APIs, submitting forms, purchasing, or changing a live system.

## Completion standard

A clone is complete only when the requested pages or flows run locally and the requested fidelity has been checked. Do not use “pixel-perfect,” “full clone,” or “exact” unless the evidence and comparison support that claim. Hand off one primary runnable deliverable plus a concise boundary note; avoid duplicate archives and junk files.
