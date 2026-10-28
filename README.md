# Fixly-Updates

**Public updater distribution channel for [Fixly Desktop](https://github.com/aryan-sonsurkar/Fixly-Desktop).**

This repository contains **only** signed auto-update artifacts published automatically by the Fixly release pipeline:

- `latest.json` - Tauri updater metadata consumed by installed Fixly clients
- `*.zip` - signed updater archives (Windows x86_64 NSIS/MSI)
- `*.sig` - minisign signatures verified against the public key embedded in the app

It intentionally contains **no source code, no installers beyond updater archives, no environment files, no credentials, and no signing keys**.

Full releases (NSIS/MSI installers, checksums, release notes) live in the [Fixly-Desktop](https://github.com/aryan-sonsurkar/Fixly-Desktop) repository. The Fixly application source remains private.

## How updates work

1. An installed Fixly client checks `latest.json` against its current version
2. If a newer version exists, the Tauri updater downloads the matching archive
3. The minisign signature is verified before installation - a bad signature aborts the update

Part of the Fixly ecosystem: [Fixly-Desktop](https://github.com/aryan-sonsurkar/Fixly-Desktop) (product) - [Fixly Website](https://github.com/aryan-sonsurkar/fixly-website) (marketing + downloads).
