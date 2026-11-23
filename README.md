[Deutsch](README.md) · [English](README.en.md)

# BigPlay – Fire-TV-Sideload-APK

**BigPlay IPTV 3.0.2 (versionCode 21)** – aus dem APKPure-XAPK (`com.bigplay.tv`, versionCode 21) zu einer **einzigen installierbaren APK** gemerged (Base + armeabi-v7a + alle Sprach-Configs + xhdpi), damit sie sich per Downloader-App direkt auf dem Fire TV installieren lässt.

## Installation (Fire TV Stick)
1. Auf dem Fire TV die App **„Downloader" (AFTVnews)** installieren.
2. Einstellungen → Mein Fire TV → Entwickleroptionen → **Apps unbekannter Herkunft installieren: Downloader → EIN**.
3. Downloader öffnen → URL eingeben:
   `https://tinyurl.com/bigplay-tv`
   (Langform: `https://github.com/FLOKHOME/bigplay-apk/releases/latest/download/BigPlay-3.0.2.apk`)
4. APK installieren; danach in der Downloader-History die Datei löschen.

## Voraussetzungen
- Fire OS 6 oder neuer (minSdk 26 = Android 8.0) → Fire TV Stick 4K (2018+), Stick 3. Gen / 4K Max, Cube. **Nicht** für alte Fire-OS-5-Sticks (2016/2017).
- CPU-Split ist **armeabi-v7a** (32 Bit) – läuft auf allen genannten Sticks.

## Hinweise
- Die APK wurde mit einem Debug-Key neu signiert → vor dem Wechsel auf eine offizielle Version die App deinstallieren (Signaturkonflikt).
- Unoffizielle persönliche Kopie zum Sideload; alle Rechte am Original liegen bei BigPlay.

Build: XAPK (APKPure, vc21) → APKEditor V1.4.9 (Merge) → zipalign + Signatur via uber-apk-signer 1.3.0.
