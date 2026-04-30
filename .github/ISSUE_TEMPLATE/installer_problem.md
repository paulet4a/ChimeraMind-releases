---
name: Installer or download problem
about: Report a broken installer, signature mismatch, antivirus block, or auto-update failure
title: "[installer] "
labels: ["installer", "triage"]
assignees: []
---

## What happened

<!-- One sentence: what went wrong? -->

## Environment

- **OS:** Windows / Linux / (macOS once supported)
- **OS version:**
- **Architecture:** x64 / arm64
- **Antivirus or endpoint protection in use:**
- **Tried installer type:** NSIS `.exe` / MSI `.msi` / AppImage / DEB

## Version

- **Tag attempted:** v3.x.y
- **`latest.json` resolved version (if known):**
- **Source URL:** `https://chimeramind.com/download` / direct GitHub release / auto-update prompt

## Symptoms

- [ ] Installer refuses to run (SmartScreen blocks even after "More info → Run anyway")
- [ ] Installer crashes mid-install
- [ ] Application launches but immediately closes
- [ ] Auto-update fails with signature error
- [ ] SHA-256 checksum does not match
- [ ] Other: <!-- describe -->

## What I expected

## Logs / screenshots

<!-- Drag-drop screenshots, paste relevant log lines. Redact secrets. -->

## Verification attempted

- [ ] Compared SHA-256 against `SHA256SUMS.txt`
- [ ] Re-downloaded the artifact
- [ ] Tried alternate installer (NSIS vs MSI)
- [ ] Confirmed antivirus is not quarantining the file
