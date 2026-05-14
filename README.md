# SymfoAmp Releases

APK release channel for **SymfoAmp**, a bit-perfect, audiophile-grade music player.

This repo only holds release artifacts (APKs + release notes). The application source lives in a separate private repo for now; it'll open up alongside the first public-release-keyed build.

## Latest

The latest beta APK is on the [Releases page](https://github.com/jayeshmann/symfoamp-releases/releases). Each release has a single attached file, `app-production-release.apk`, plus full notes describing what's new since the previous release.

## Install on Android

These APKs are **debug-signed for friends-and-family distribution**. A release signing key + Play Store listing is tracked separately. To install:

1. **Allow installs from your browser.** Settings -> Apps -> Special access -> Install unknown apps -> (the browser you'll download with) -> Allow.
2. **Download the latest `app-production-release.apk`** from the [Releases page](https://github.com/jayeshmann/symfoamp-releases/releases/latest).
3. **Bypass Play Protect.** Google Play Protect flags the APK as "harmful" because it isn't from the Play Store. Tap **Install anyway** (sometimes hidden under **More details**).
4. Open SymfoAmp. The version under Settings -> About should match the release tag you installed.

## Want to report a bug?

From inside the app: Settings -> Diagnostics -> **Send feedback**. The form attaches the last bit of in-app log to help diagnose. There's no account tie, no IP retention.

If the app can't open at all, you can still file a GitHub issue against this repo — describe the symptom + your device model + the version that broke.

## Build targets

- **Android** 14+ (API 34). Tested on Pixel 9 (API 36).
- **iOS / macOS / Windows** are in the build pipeline but not published here yet.
- **Linux is not a ship target.**

## License

The published APKs are for evaluation by invited testers. All rights reserved on the application code. The app embeds open-source components; their licenses ship inside the APK and are visible through Settings -> About once that menu lands.
