# FamilyMap

- `familymap-backend/` — Node.js + Express + MongoDB API
- `familymap_app/` — Flutter app (web / Android / iOS)

## Requirements

| Tool | Version |
|---|---|
| Node.js | 18+ |
| MongoDB | 6+ |
| Flutter | 3.11+ |

## Backend

```bash
cd familymap-backend
npm install
cp .env.example .env       # then set MONGO_URI, JWT_SECRET, JWT_REFRESH_SECRET
npm run seed               # optional: admin@familymap.lv / Admin123!
npm run dev                # http://localhost:5001
```

## Flutter app

Set `apiBaseUrl` in `familymap_app/lib/config.dart` (use `10.0.2.2` for Android emulator, LAN IP for a physical device).

```bash
cd familymap_app
flutter pub get
flutter run -d chrome       # web
flutter run -d ios          # iOS simulator
flutter run -d android      # Android emulator/device
```

## Build

```bash
flutter build web           # → build/web
flutter build apk           # Android
flutter build ios           # iOS (macOS + Xcode)
```
