# 🏟️ GuruTournaments v1.0.0 – Stadium Edition

**Release Date:** 31.10.2025  
**Repository:** [GuruGroup-de/guru_tournaments](https://github.com/GuruGroup-de/guru_tournaments)  
**Build Type:** Production – Flutter 3.24.0 + Firebase  
**Maintainer:** Ventsislav Georgiev (GuruGroup, Germany)

---

## ✨ Overview
GuruTournaments 1.0.0 introduces a complete, production-ready tournament management system for modern football coaches and organizers.  
Built entirely with **Flutter + Firebase**, this release includes advanced features like live Scoreboard TV Mode, version control, feedback reporting, and a brand-new stadium-themed landing page.

---

## ⚙️ New Features

### 🏟️ 1. Scoreboard TV Mode
- Full-screen responsive view (1xN, 2xN, 3xN)
- Stadium dark gradient (#0C1220 → #1E3C72)
- WakeLock enabled (no sleep)
- Keyboard controls: **N**, **P**, **F**
- Real-time Firestore match updates
- Team badges, status indicators, tabular font scores

### 🧠 2. App Version Control
- Firestore: `config/app`
- Force update & optional update
- Changelog + APK URL
- Local vs remote version comparison

### 💬 3. In-App Feedback System
- Firestore: `feedback/{ticketId}`
- Optional diagnostics (device, OS, screen, version)
- Auto-generated ticket IDs
- Admin access panel

### 🔐 4. Firestore Security Rules
- Role-based writes (`admin`, `coach`, `viewer`)
- Public read for tournaments/matches
- Authenticated user feedback write
- Admin-only analytics/config write

### 🌐 5. Website Landing Page
- `/docs/index.html` stadium theme
- Hero • Features • Screenshots • Download sections
- CTA Buttons: *View on GitHub* / *Download PDF Checklist*
- Responsive and hosted via GitHub Pages

---

## 🧩 Technical Summary
| Category | Detail |
|-----------|---------|
| Total Dart Files | **70** |
| New Features | **5 major** |
| New Services | **2** |
| Firestore Rules | **95 lines** |
| Dependencies | `wakelock_plus: ^1.3.3` |
| Lint Status | ✅ 0 Errors |
| Architecture | Layered (features, services, shared) |
| Docs | `NEW_FEATURES_IMPLEMENTATION.md` |

---

## 🧾 Documentation
- 📘 [GuruTournaments Docs](https://gurugroup-de.github.io/guru_tournaments/)
- 🧠 [NEW_FEATURES_IMPLEMENTATION.md](https://github.com/GuruGroup-de/guru_tournaments/blob/main/NEW_FEATURES_IMPLEMENTATION.md)
- 📄 [Deploy Checklist PDF](https://gurugroup-de.github.io/guru_tournaments/docs/GuruTournaments_Deploy_Checklist.pdf)

---

## 🚀 Pending for v1.1
- Admin Dashboard v2 (fl_chart)
- Firebase Crashlytics
- Offline caching improvements
- Accessibility & UX polish
- Integration test suite
- Build flavors: dev/staging/prod

---

## 💡 How to Update
```bash
git pull origin main
flutter build apk --release
flutter build web --release
```
Update Firestore config/app → `androidVersion: 2`, `forceUpdate: false`

---

## 📦 Assets
| File | Description |
|------|--------------|
| `GuruTournaments_Deploy_Checklist.pdf` | Deploy guide |
| `/docs/index.html` | Landing page |
| `/docs/screenshots/` | UI images |
| `/lib/features/scoreboard/` | Scoreboard module |
| `/lib/services/version_service.dart` | Version logic |
| `/lib/services/feedback_service.dart` | Feedback logic |

---

## 🧑‍💻 Credits
Developed by **Ventsislav Georgiev**  
Part of the **CoachGuru Ecosystem** • Germany 🇩🇪  
GitHub: [GuruGroup-de](https://github.com/GuruGroup-de)  
Website: [coachguru-app.github.io](https://coachguru-app.github.io/CoachGuru/)

---

## 🔖 Tag This Release
```bash
git tag -a v1.0.0 -m "GuruTournaments v1.0.0 – Stadium Edition"
git push origin v1.0.0
```
