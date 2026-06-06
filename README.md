# CSI Bridge — Releases

Public auto-update feed for the **CSI Bridge** desktop app — the macOS menu-bar
connector that relinks proxies to original media and launches NLEs for
[CSI (Creative Space Intelligence)](https://creative.space).

This repository holds **only signed + notarized release binaries**. The
application source lives in the private CSI repo. Updates here are consumed
automatically by every installed Bridge via
[electron-updater](https://www.electron.build/auto-update).

## Two-prong update feed

Each Bridge checks two sources, in order, and falls back automatically:

1. **GitHub Releases** (this repo) — public CDN, always reachable.
2. **CSI server** (`/bridge-updates`) — internal / on-prem feed served from the appliance.

## Install

Grab the latest `.dmg` from **[Releases](../../releases/latest)**. After the first
install the Bridge keeps itself current — you'll get a one-click
**"Relaunch to update"** whenever a new version ships.

## How releases are published

CI builds on a `bridge-v*` tag: **build → sign (Developer ID) → notarize → publish
here + mirror to the CSI server**. See `.github/workflows/bridge-release.yml` in
the main repo.

---
© DigitalGlue · CSI
