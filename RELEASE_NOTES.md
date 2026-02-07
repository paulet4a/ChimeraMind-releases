# ChimeraMind v2.0.0 - Major Release

**Release Date:** February 7, 2026

---

## 🚀 Architecture Overhaul

### Event-Driven Architecture
- Complete rewrite from FSM to event-driven system
- ModuleRegistry with dependency-ordered startup
- EventBus with 8 async workers for inter-module communication
- 9 core modules: Data, ModelInference, FeatureAggregation, Decision, Risk, Trading, Execution, Monitoring, Metrics

### Cloud Deployment
- Production backend on OVHcloud VPS (Germany)
- 10 Docker containers running 24/7
- Real-time paper trading with Binance
- Redis event bus for distributed communication

### Master-Worker Architecture
- Master engine: 9 modules (decisions, risk, execution)
- Worker engine: 3 modules (data, inference, features)
- Horizontal scaling ready

---

## 🔧 New Features

### Live Trading Dashboard
- Real-time BTC/ETH/SOL/BNB/XRP price ticker
- WebSocket live data streaming
- Decision Council with AI verdict system
- Cortex & Hunter status indicators

### Cloud API
- FastAPI backend at `http://51.195.109.14:8000`
- Paper trading mode with full order simulation
- Walk-forward analysis endpoints
- System health monitoring

### Desktop App
- Cyberpunk-themed UI with dark mode
- Tauri 2.x secure sandbox
- Auto-updater support
- System tray integration

---

## 📦 Installation

### Windows (Recommended)
Download: `ChimeraMind_2.0.0_x64-setup.exe`
- Double-click to install
- No administrator privileges required

---

## 📊 Technical Details

| Metric | Value |
|--------|-------|
| Build Size | ~4MB (installer) |
| Backend RAM | 3.4 GB / 12 GB |
| Docker Services | 10 containers |
| Supported Symbols | BTC, ETH, SOL, BNB, XRP |
| Trading Mode | Paper (default) |

---

## 📝 Known Issues

1. **Auto-update**: v1.x users must manually install v2.0.0 (signing key changed)
2. **Trade History**: Portfolio page may timeout if no trades exist yet
3. **Telegram Bot**: Requires TELEGRAM_TOKEN in .env

---

## 📞 Support

For issues and feature requests:
- GitHub Issues: https://github.com/paulet4a/ChimeraMind-releases/issues

---

**Full Changelog**: See CHANGELOG.md
