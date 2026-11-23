[Deutsch](README.md) · [English](README.en.md)

# BigPlay – Fire TV Sideload APK

**BigPlay IPTV 3.0.2 (versionCode 21)** – merged from the APKPure XAPK (`com.bigplay.tv`, versionCode 21) into a **single installable APK** (base + armeabi-v7a + all language configs + xhdpi) so it can be installed directly on a Fire TV using the Downloader app.

## Installation (Fire TV Stick)
1. Install the **"Downloader" app (AFTVnews)** on the Fire TV.
2. Settings → My Fire TV → Developer options → **Install unknown apps: Downloader → ON**.
3. Open Downloader → enter URL:
   - **Fire OS 7** (Stick 2021/3rd gen, 4K Max, Cube 2nd gen): `https://tinyurl.com/bigplay-tv`
   - **Fire OS 6** (Stick 4K 2018, Cube 1st gen): `https://tinyurl.com/bigplay-fos6` ← patched variant `BigPlay-3.0.2-vc21-minSdk23.apk` (minSdk 23, see below)
4. Install the APK; delete the file from Downloader's history afterwards.

## Requirements
- BigPlay original: Fire OS 7+ (minSdk 26 = Android 8.0) → Fire TV Stick 3rd gen/4K Max/Lite, Cube 2nd gen. The official app was **never** installable on Fire OS 6 (4K Stick 2018, API 25) – all versions 1.x–3.x require minSdk 26.
- Fire OS 6 → only with the patched variant (`-vc21-minSdk23`): minSdk 23, adaptive icons moved to v26, `startForegroundService` guarded with an SDK-26 check (WorkManager), `extractNativeLibs=true`, **PairIP license check removed** (Fire TV has no Play licensing service – the original APK dies at startup on Fire TV regardless of signature). Remaining risk: the notification/EPG-reminder path uses channel APIs without a guard → may crash on Android 7 if you use EPG reminders.
- The CPU split is **armeabi-v7a** (32-bit) – runs on all of the above.

## Notes
- The APK was re-signed with a debug key → uninstall the app before switching to an official build (signature conflict).
- Unofficial personal copy for sideloading; all rights to the original belong to BigPlay.

Build: XAPK (APKPure, vc21) → APKEditor V1.4.9 (merge) → zipalign + signature via uber-apk-signer 1.3.0.
