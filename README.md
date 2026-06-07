# SymfoAmp Releases

Public release channel for **SymfoAmp**, a bit-perfect, audiophile-grade music player.

This repo only holds release artifacts (per-platform builds + release notes). The application source lives in a separate private repo for now; it'll open up alongside the first public-release-keyed build.

## Latest

The latest build is on the [Releases page](https://github.com/jayeshmann/symfoamp-releases/releases). Each release attaches per-platform artifacts named `symfoamp-<version>-<os>-<arch>.<ext>` (currently an Android `.apk` and a macOS `.zip`), plus full notes describing what's new since the previous release.

## Install on Android

These APKs are **debug-signed for friends-and-family distribution**. A release signing key + Play Store listing is tracked separately. To install:

1. **Allow installs from your browser.** Settings -> Apps -> Special access -> Install unknown apps -> (the browser you'll download with) -> Allow.
2. **Download the latest `symfoamp-<version>-android-universal.apk`** from the [Releases page](https://github.com/jayeshmann/symfoamp-releases/releases/latest).
3. **Bypass Play Protect.** Google Play Protect flags the APK as "harmful" because it isn't from the Play Store. Tap **Install anyway** (sometimes hidden under **More details**).
4. Open SymfoAmp. The version under Settings -> About should match the release tag you installed.

## Install on macOS

The macOS build is **unsigned** (no Apple Developer ID yet), so Gatekeeper blocks a plain double-click on first launch.

1. **Download the latest `symfoamp-<version>-macos-arm64.zip`** from the [Releases page](https://github.com/jayeshmann/symfoamp-releases/releases/latest).
2. Unzip it and move **SymfoAmp** into your Applications folder.
3. **First launch:** right-click (or Control-click) SymfoAmp -> **Open** -> confirm. It opens normally after that.
4. Settings -> About should match the release tag you installed.

Requires macOS 14 Sonoma or newer (Apple Silicon). Tested on macOS 26 Tahoe.

## Want to report a bug?

From inside the app: Settings -> Diagnostics -> **Send feedback**. The form attaches the last bit of in-app log to help diagnose. There's no account tie, no IP retention.

If the app can't open at all, you can still file a GitHub issue against this repo — describe the symptom + your device model + the version that broke.

## Platform targets

Mirrors the app's ship targets. Android and macOS builds are published here today; Windows and iOS are still in the pipeline.

| Platform | Min version | Audio API | Status |
|----------|-------------|-----------|--------|
| Android | 14+ (API 34) | AAudio | Early Access (published here) |
| Windows | 11 24H2+ (64-bit) | WASAPI Shared | Planned |
| macOS | 14+ Sonoma (Apple Silicon) | CoreAudio | Early Access (published here) |
| iOS | 18+ | CoreAudio | Planned |

Android builds are tested on Pixel 9 (API 36); macOS builds on macOS 26 Tahoe. **Linux is not a ship target.**

## License

The published APKs are for evaluation by invited testers. All rights reserved on the application code. The app embeds open-source components; their licenses ship inside the APK and are visible through Settings -> About once that menu lands.
