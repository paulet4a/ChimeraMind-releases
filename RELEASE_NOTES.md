# ChimeraMind v1.3.5 - Release Notes

**Release Date:** January 31, 2026

---

## 🚀 Performance Optimizations

### Bundle Optimization
- **50% smaller initial load** (~800KB → ~400KB)
- Feature-based code splitting (manual chunks)
- Optimized dependency pre-bundling

### Lazy Loading
- **CopilotChat**: Loaded on-demand (saves ~15KB on startup)
- **3D Components**: Loaded only in 3D-Hub (saves ~500KB)
- **ActivityLog**: Lazy loaded with Intersection Observer (saves ~5KB)

### Prefetch Strategy
- Critical chunks preloaded in background
- DNS prefetch for external resources
- Faster page transitions

---

## 🔧 New Features

### Service Worker (Offline Support)
- Full offline cache capability
- Background sync (30-minute intervals)
- Three cache strategies:
  - **Cache First**: JS/CSS chunks
  - **Network First**: HTML pages
  - **Stale While Revalidate**: Fonts

### Intersection Observer
- Smart component loading
- Reduces initial render time
- Shimmer placeholder effects

### Font Loading Optimization
- `font-display: swap` prevents FOIT
- Removed unused fonts
- Preconnect to Google Fonts

---

## 🐛 Bug Fixes

- Removed duplicate `sound.ts` service
- Cleaned up debug console.log statements
- Fixed TradingChart ResizeObserver memory leak
- Updated all sound imports to use `sounds`

---

## 📦 Installation

### Windows (Recommended)
Download: `ChimeraMind_1.3.5_x64-setup.exe`
- Double-click to install
- No administrator privileges required
- Auto-updater included

### Windows (MSI)
Download: `ChimeraMind_1.3.5_x64_en-US.msi`
- System-wide installation
- Suitable for enterprise deployment

---

## 📊 Technical Details

| Metric | Value |
|--------|-------|
| Build Size | ~4MB (installer) |
| Runtime Memory | ~100MB |
| Startup Time | <2 seconds |
| Offline Support | ✅ Yes |

---

## 🔐 Security

- CSP (Content Security Policy) enabled
- Localhost API proxy for secure communication
- Tauri 2.x secure sandbox

---

## 📝 Known Issues

1. **First Launch**: May take 2-3 seconds for initial cache setup
2. **3D Mode**: Requires WebGL 2.0 support
3. **Offline Mode**: Real-time data requires internet connection

---

## 🔄 Auto-Updater

This version includes auto-updater. When a new version is available:
1. Notification will appear
2. Click "Download & Install"
3. Application will restart automatically

---

## 📞 Support

For issues and feature requests:
- GitHub Issues: https://github.com/paulet4a/ChimeraMind-releases/issues

---

**Full Changelog**: See CHANGELOG.md
