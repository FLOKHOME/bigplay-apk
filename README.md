[Deutsch](README.md) · [English](README.en.md)

# BigPlay – Fire-TV-Sideload-APK

**BigPlay IPTV 3.0.2 (versionCode 21)** – aus dem APKPure-XAPK (`com.bigplay.tv`, versionCode 21) zu einer **einzigen installierbaren APK** gemerged (Base + armeabi-v7a + alle Sprach-Configs + xhdpi), damit sie sich per Downloader-App direkt auf dem Fire TV installieren lässt.

## Installation (Fire TV Stick)
1. Auf dem Fire TV die App **„Downloader" (AFTVnews)** installieren.
2. Einstellungen → Mein Fire TV → Entwickleroptionen → **Apps unbekannter Herkunft installieren: Downloader → EIN**.
3. Downloader öffnen → URL eingeben:
   - **Fire OS 7** (Stick 2021/3. Gen, 4K Max, Cube 2. Gen): `https://tinyurl.com/bigplay-tv`
   - **Fire OS 6** (Stick 4K 2018, Cube 1. Gen): `https://tinyurl.com/bigplay-fos6` ← gepatchte Variante `BigPlay-3.0.2-vc21-minSdk23.apk` (minSdk 23, siehe unten)
4. APK installieren; danach in der Downloader-History die Datei löschen.

## Voraussetzungen
- BigPlay original: Fire OS 7+ (minSdk 26 = Android 8.0) → Fire TV Stick 3. Gen/4K Max/Lite, Cube 2. Gen. Die offizielle App war **nie** für Fire OS 6 (4K-Stick 2018, API 25) installierbar – alle Versionen 1.x–3.x setzen minSdk 26.
- Fire OS 6 → nur mit der gepatchten Variante (`-vc21-minSdk23`): minSdk 23, adaptive Icons nach v26 verschoben, `startForegroundService` mit SDK-26-Guard (WorkManager) versehen, `extractNativeLibs=true`. Restrisiko: Benachrichtigungs-/EPG-Erinnerungspfad nutzt Channel-APIs ohne Guard → kann auf Android 7 abstürzen, wenn EPG-Erinnerungen genutzt werden.
- CPU-Split ist **armeabi-v7a** (32 Bit) – läuft auf allen genannten Sticks.

## Hinweise
- Die APK wurde mit einem Debug-Key neu signiert → vor dem Wechsel auf eine offizielle Version die App deinstallieren (Signaturkonflikt).
- Unoffizielle persönliche Kopie zum Sideload; alle Rechte am Original liegen bei BigPlay.

Build: XAPK (APKPure, vc21) → APKEditor V1.4.9 (Merge) → zipalign + Signatur via uber-apk-signer 1.3.0.
