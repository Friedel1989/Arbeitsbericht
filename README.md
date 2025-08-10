# Entstörprotokoll Wizard – PWA + Capacitor (Android APK via GitHub Actions)

Funktionen:
- Ein Feld pro Schritt
- Fotos anhängen
- Signatur (Finger/Stift)
- PDF aus Vorlage (Form-Felder + Bilder + Unterschrift)
- E-Mail am Schluss (Share Sheet / mailto)
- Offlinefähig

## Lokal starten
```bash
npm install
npm run dev
```

## Build
```bash
npm run build
```

## Android (lokal)
Voraussetzung: Android SDK/Gradle.
```bash
npm run build
npx cap sync android
cd android
./gradlew assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

## Android APK per GitHub Actions (empfohlen)
1. Repo bei GitHub anlegen, Code pushen.
2. Workflow erzeugt eine Debug-APK als Artefakt.

APK danach in Actions → letzter Lauf → Artifacts herunterladen.

