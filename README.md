# Universal Clone

A Codex skill that routes website and app cloning work through the lowest-cost suitable workflow.

It supports:

- Static websites and SPAs through `decant`
- Interactive frontend reconstruction
- Electron, APK, native, and packaged-app investigation through REA
- Screenshot-based UI reconstruction
- Evidence-labelled verification: Verified, Observed, Inferred, Mocked, and Unknown

The skill asks only the questions that materially affect the clone: desired outcome, scope, and target type. It does not claim to recover unseen backends, databases, private APIs, or production data.

## Install

Copy or clone this repository to:

```text
~/.codex/skills/universal-clone
```

Then invoke it with:

```text
Use $universal-clone to clone https://example.com as a functional local prototype.
```

## Optional runtimes

- `decant` for efficient website capture and design-token extraction
- `reverse-engineer-anything` / REA for shipped application analysis
- `url-to-code` when the Product Design environment is available
- `design-mirror` when Bright Data is already configured

The default route starts with free local tools and the smallest useful capture to reduce model usage.
