<div align="center">

# ChimeraMind — Desktop Releases

**AI-powered crypto futures execution platform. Paper-first, governed rollout.**

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

## Install

### Windows

1. Download `ChimeraMind_<version>_x64-setup.exe` from the latest release.
2. Run the installer.
3. Windows SmartScreen may show **"Windows protected your PC"** — this is expected for newly published binaries that have not yet built a Microsoft reputation score. Click **More info → Run anyway**. The Microsoft Store / signed-MSIX path is on the post-beta roadmap.
4. Sign in with your ChimeraMind account.

### Linux

1. Download the `.AppImage` from the latest release.
2. `chmod +x ChimeraMind_<version>_amd64.AppImage`
3. Run it.

## Auto-Update

ChimeraMind ships with a Tauri 2 updater that:

- Polls `latest.json` on app start and on a periodic timer.
- Downloads + verifies the signed update payload (Ed25519, see `*.sig` artifacts).
- Prompts the user before applying the update.

`latest.json` (this repo root) is the authoritative manifest — updater never trusts arbitrary HTTPS sources.

## Signature Verification

Every release artifact is paired with a `.sig` file (Ed25519, Tauri updater format). The desktop updater rejects any payload whose signature does not match the embedded public key. If you want to manually verify a download, use Tauri's [`signtool verify`](https://v2.tauri.app/distribute/sign/) workflow against the `.sig` next to the binary.

## What is ChimeraMind?

A multi-strategy crypto futures execution platform built for traders who care about **process** as much as outcome:

- **21 trading bots** across scalping, momentum, mean-reversion, breakout, and event-driven categories.
- **8 enhancers** — antifragile barbell, Kelly cap, regime-aware sizing, liquidation-aware entries.
- **AI cortex** — GBM direction model + HMM regime detection + DeepLOB micro-structure + RL agent + Cascade veto.
- **Real-time analytics** — VPIN, CVD, OI velocity, funding-rate divergence, whale flow, on-chain hunter, factor alpha.
- **Paper-first** — every new bot, every new enhancer ships in paper mode by default. Live mode is per-account, opt-in, gated, and governed.

Full overview: <https://chimeramind.com>

## Support & Links

- Product site: <https://chimeramind.com>
- Status & changelog: see [**Releases**](https://github.com/paulet4a/ChimeraMind-releases/releases)
- Updates: [@ChimeraMindApp](https://x.com/ChimeraMindApp)

## License

Desktop binaries are distributed under the ChimeraMind end-user license. The application source code lives in a separate, private repository; this repository hosts release artifacts only.

<div align="center">
<sub>ChimeraMind — paper-mode default. Live trading is opt-in and governed.</sub>
</div>
