# Liquid Glass Icons v2.0 — Ultra Gloss

An Android liquid-glass icon pack with **637 built-in icon designs**, a searchable icon gallery, and an on-device icon glassifier for launchable apps that are not included in the built-in collection.

Built for compatible third-party Android launchers, including **Smart Launcher**. Automatic icon application depends on the launcher and each app's component mapping; the APK has 117 predefined launcher mappings. Unmapped apps can be glassified and exported as PNGs for manual assignment.

## Build the Android APK on GitHub

Upload these **three ZIP files** to the **root of the repository**, without extracting them:

- `liquidglass-source-01.zip`
- `liquidglass-source-02.zip`
- `liquidglass-source-03.zip`

You can use [GitHub's upload page](https://github.com/Wayudiesa24/LiquidGlassIcons/upload/main). Upload all three together, then select **Commit changes**.

The workflow under `.github/workflows/build-apk.yml` runs when the archive files are uploaded. You can also use **Actions → Build Android APK → Run workflow** once all three archives exist.

When the build succeeds: open the workflow run, download the **LiquidGlassIcons-v2-APK** artifact, unzip it, and install `app-debug.apk` on your Android phone. This is a debug APK for personal testing, not a signed Play Store release.

## Design

Ultra-glossy translucent glass tiles with refractive edges and vibrant symbols. The 637 PNG/SVG designs cover 14 categories. Some are visual category interpretations rather than identical representations of brand logos.

## Compatibility and privacy

- Requires Android 8.0+.
- Compatible launcher support needs on-device verification.
- 117 built-in component mappings mean not every app is automatically replaced.
- Glassify My Installed Apps exports manually assignable PNGs from the installed app's original launcher icon.
- No internet, ad, account, or broad storage permission is needed by the Android app itself.

Source archives are intentionally ZIPs to keep mobile uploads manageable. The GitHub Actions runner extracts them before compiling with Java 17, Gradle 8.10.2, Android Gradle Plugin 8.7.3 and Android SDK 35.
