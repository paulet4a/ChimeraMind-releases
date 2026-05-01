<div align="center">

# ChimeraMiND — Desktop Releases

**Trading, reimagined as an organism.**
21 strategies as one antifragile mind. Adaptive. Governed. Audit-grade.

[![Latest](https://img.shields.io/github/v/release/paulet4a/ChimeraMind-releases?style=for-the-badge&label=Latest&color=10B981)](https://github.com/paulet4a/ChimeraMind-releases/releases/latest)
[![Website](https://img.shields.io/badge/chimeramind.com-00E5FF?style=for-the-badge&logo=googlechrome&logoColor=white)](https://chimeramind.com)
[![X](https://img.shields.io/badge/@ChimeraMindApp-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/ChimeraMindApp)

</div>

---

## Download

Get the latest desktop build from the [**Releases**](https://github.com/paulet4a/ChimeraMind-releases/releases/latest) page.

| Platform | Installer |
|----------|-----------|
| Windows x64 | `ChimeraMind_<version>_x64-setup.exe` (NSIS) or `ChimeraMind_<version>_x64_en-US.msi` |
| Linux x64 | `ChimeraMind_<version>_amd64.AppImage` |

> Recommended path for new users: <https://chimeramind.com/download> — picks the right artifact for your OS and walks you through onboarding.

> Installer file names keep the lowercase `ChimeraMind_*` form for Tauri auto-updater compatibility. The brand display name is stylized **ChimeraMiND** elsewhere.

## Install

### Windows

1. Download `ChimeraMind_<version>_x64-setup.exe` from the latest release.
2. Run the installer.
3. Windows SmartScreen may show **"Windows protected your PC"** — this is expected for newly published binaries that have not yet built a Microsoft reputation score. Click **More info → Run anyway**. The Microsoft Store / signed-MSIX path is on the post-beta roadmap.
4. Sign in with your ChimeraMiND account.

### Linux

1. Download the `.AppImage` from the latest release.
2. `chmod +x ChimeraMind_<version>_amd64.AppImage`
3. Run it.

## Auto-Update

ChimeraMiND ships with a Tauri 2 updater that:

- Fetches `latest.json` (this repo's `main` branch root, also proxied via `https://chimeramind.com/latest.json`).
- Verifies the signed update payload (Ed25519, see `*.sig` artifacts).
- Prompts the user before applying the update.

`latest.json` is the authoritative manifest — the updater never trusts arbitrary HTTPS sources.

## Verify Downloads

Every release is paired with `SHA256SUMS.txt` and per-asset `.sig` files (Ed25519, Tauri updater format). Verify before running.

### SHA-256

**Windows (PowerShell):**
```powershell
Get-FileHash .\ChimeraMind_<version>_x64-setup.exe -Algorithm SHA256
# compare against the matching line in SHA256SUMS.txt
```

**Linux / macOS:**
```bash
sha256sum -c SHA256SUMS.txt --ignore-missing
```

### Signature

The desktop updater rejects any payload whose Ed25519 signature does not match the embedded public key. To verify manually, see Tauri's [`signtool verify`](https://v2.tauri.app/distribute/sign/) workflow against the `.sig` next to each binary.

## What is ChimeraMiND?

A multi-strategy crypto futures execution platform built for traders who care about **process** as much as outcome:

- **21 trading bots** across scalping, momentum, mean-reversion, breakout, and event-driven categories.
- **8 enhancers** — antifragile barbell, Kelly cap, regime-aware sizing, liquidation-aware entries.
- **AI cortex** — GBM direction + HMM regime + DeepLOB micro-structure + RL agent + Cascade veto.
- **Real-time analytics** — VPIN, CVD, OI velocity, funding-rate divergence, whale flow, on-chain hunter, factor alpha.
- **Paper-first** — every new bot, every new enhancer ships in paper mode by default. Live mode is per-account, opt-in, gated, and governed.

Full overview: <https://chimeramind.com>

## Support & Links

- Product site: <https://chimeramind.com>
- Status & changelog: see [**Releases**](https://github.com/paulet4a/ChimeraMind-releases/releases)
- Updates: [@ChimeraMindApp](https://x.com/ChimeraMindApp)
- LinkedIn: [chimeramind](https://www.linkedin.com/company/chimeramind/)
- Security disclosures: `security@chimeramind.com` (see [SECURITY.md](SECURITY.md))

## License

Desktop binaries are distributed under the ChimeraMiND end-user license (see [LICENSE](LICENSE)). The application source code lives in a separate, private repository; this repository hosts release artifacts only.

<div align="center">
<sub>Paper-mode default. Live trading is opt-in and governed.</sub>
</div>
