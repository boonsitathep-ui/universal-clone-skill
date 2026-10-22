# Routing

Choose one primary route, then add a secondary route only for a concrete gap.

## Website or web app

### Offline mirror or asset capture

Use `decant`.

1. Start with `decant clone <url> --depth 0 --rate-limit 2 --concurrency 4 --output <new-dir>`.
2. Inspect `repair-hints.json`, `context.md`, `manifest.json`, and `design-tokens.json`.
3. If the page is client-rendered or missing runtime assets, rerun with `--render chrome --runtime-capture auto`.
4. Increase crawl depth only when the requested scope requires linked pages.
5. Use authenticated capture only with explicit authorization and keep cookies outside the deliverable.

This route preserves frontend resources; it does not reproduce backend behavior.

### Faithful interactive frontend

Use `url-to-code` when the Product Design workflow and browser surface are available. Otherwise inspect with browser automation, implement in the user's stack, and compare rendered screenshots. Preserve the user's framework when cloning into an existing repository.

### Design language only

Use `design-mirror` for tokens and styling, not content or behavior. It requires configured Bright Data credentials; do not introduce that paid dependency when `decant` or browser inspection is sufficient.

## Source repository

Use normal repository inspection and implementation. Do not use reverse engineering merely because the result is an application. Read the repository's instructions, preserve unrelated changes, identify entry points and data contracts, then implement and test in the existing stack.

## Electron or packaged JavaScript app

Use `reverse-engineer-anything` with `analyze_javascript_application` for ASAR or extracted JavaScript, and runtime observation only when static evidence leaves a material gap. Separate packaged observations from runtime observations.

## Android APK

Use REA package inspection first. Inventory declarations, screens, classes, resources, and network contracts relevant to the requested flow. Rebuild with new source; do not copy secrets, signing material, protected services, or third-party data.

## Native or managed desktop app

Use REA on the supplied artifact. Start with overview/inventory and investigate only requested features. Static analysis is not execution evidence. Build a clean-room implementation from documented behavior and permitted assets.

## Screenshot, recording, or inaccessible target

Build only what the visual evidence supports. Ask for missing screens or interaction outcomes when they materially affect the result. Mark hidden states, data rules, responsive behavior, accessibility, and backend behavior as unknown until observed.

## Recommended user question

When outcome is ambiguous, ask:

“ต้องการแบบไหน: (1) Mirror เปิด offline, (2) Clone หน้าตาและ interaction, (3) Prototype ที่ใช้ mock data, หรือ (4) วิเคราะห์แอปแล้วสร้างฟังก์ชันใหม่? และต้องการทั้งระบบหรือเฉพาะหน้าหรือ flow ไหน?”

