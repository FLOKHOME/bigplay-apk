[Deutsch](README.md) · [English](README.en.md)

# BigPlay – Fire TV Sideload APK

**BigPlay IPTV 3.0.2 (versionCode 21)** – merged from the APKPure XAPK (`com.bigplay.tv`, versionCode 21) into a **single installable APK** (base + armeabi-v7a + all language configs + xhdpi) so it can be installed directly on a Fire TV using the Downloader app.

## Installation (Fire TV Stick)
1. Install the **"Downloader" app (AFTVnews)** on the Fire TV.
2. Settings → My Fire TV → Developer options → **Install unknown apps: Downloader → ON**.
3. Open Downloader → enter URL:
   `https://tinyurl.com/bigplay-tv`
   (Long form: `https://github.com/FLOKHOME/bigplay-apk/releases/latest/download/BigPlay-3.0.2.apk`)
4. Install the APK; delete the file from Downloader's history afterwards.

## Requirements
- Fire OS 6 or newer (minSdk 26 = Android 8.0) → Fire TV Stick 4K (2018+), Stick 3rd gen / 4K Max, Cube. **Not** for older Fire OS 5 sticks (2016/2017).
- The CPU split is **armeabi-v7a** (32-bit) – runs on all of the above.

## Notes
- The APK was re-signed with a debug key → uninstall the app before switching to an official build (signature conflict).
- Unofficial personal copy for sideloading; all rights to the original belong to BigPlay.

Build: XAPK (APKPure, vc21) → APKEditor V1.4.9 (merge) → zipalign + signature via uber-apk-signer 1.3.0.
