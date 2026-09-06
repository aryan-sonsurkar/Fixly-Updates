# Fixly-Updates

Public updater distribution artifacts for **Fixly Desktop**.

This repository contains **only** signed auto-update artifacts published automatically by the private `Fixly-Desktop` release pipeline:

- `latest.json` — Tauri updater metadata consumed by installed Fixly clients
- `*.zip` — signed updater archives (Windows x86_64 NSIS/MSI)
- `*.sig` — minisign signatures verified against the public key embedded in the app

It intentionally contains **no source code, no installers beyond updater archives, no environment files, no credentials, and no signing keys**.

Full releases (NSIS/MSI installers, checksums, release notes) live in the private `Fixly-Desktop` repository. The Fixly application source remains private.
