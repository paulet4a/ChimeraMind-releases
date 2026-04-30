# Security Policy — ChimeraMind Desktop Releases

This repository hosts the signed desktop binaries for [ChimeraMind](https://chimeramind.com).

## Reporting a Vulnerability

- **Email:** `security@chimeramind.com`
- **Subject prefix:** `[security]` plus a one-line summary
- **Do not** open public issues for security findings.

### Scope of this repository

- Desktop binaries (Windows NSIS / MSI, Linux AppImage / DEB)
- Ed25519 signatures (`*.sig`)
- `latest.json` update manifest
- `SHA256SUMS.txt` checksum file

### What to report here

- A binary fails Ed25519 signature verification
- `latest.json` points at a payload whose signature does not match
- A SHA-256 checksum mismatch
- A release artifact contains unexpected files
- Auto-updater behaves unexpectedly when fed a crafted manifest

### Response SLA

| Stage | Target |
|-------|--------|
| Initial acknowledgement | 48 hours |
| Triage + severity assigned | 7 days |
| Fix or mitigation deployed | 30 days for high/critical, 90 days otherwise |
| Public disclosure | Coordinated, after fix is adopted |

### Out of scope here

Application-logic vulnerabilities (auth, billing, trading, exchange-key handling) — please report those via the same `security@chimeramind.com` channel; they will be triaged against the private application repository.

## Verification Workflow

Every release is paired with:

- `*.sig` — Ed25519 signature, Tauri updater format
- `SHA256SUMS.txt` — SHA-256 hashes of each artifact

### Windows (PowerShell)

```powershell
Get-FileHash .\ChimeraMind_<version>_x64-setup.exe -Algorithm SHA256
# Compare against the line in SHA256SUMS.txt
```

### Linux / macOS

```bash
sha256sum -c SHA256SUMS.txt --ignore-missing
```

The desktop application's auto-updater enforces signature verification automatically — a tampered binary will be rejected before installation.

Thank you for helping keep ChimeraMind users safe.
