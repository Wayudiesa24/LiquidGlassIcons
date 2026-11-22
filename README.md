# Liquid Glass Icons — v2.0 Ultra Gloss

A **native Android icon-pack app** featuring 637 ultra-glossy, translucent icons, a searchable gallery, 14 categories, 117 explicit launcher component mappings, and a built-in **Glassify My Installed Apps** tool for apps outside the predefined set.

## Download the Android APK

1. Open the [GitHub Actions build page](https://github.com/Wayudiesa24/LiquidGlassIcons/actions/workflows/build-apk.yml).
2. Open the most recent successful **Build Android APK** run.
3. Under **Artifacts**, download `LiquidGlassIcons-v2-APK`.
4. Extract the artifact ZIP and install `app-debug.apk` on your Android phone.

This is an Android **debug-signed APK** for personal testing, not a Play Store release. Android 8.0 or later is required.

## Apply with Smart Launcher

Install the APK, then open Smart Launcher settings and find its icon pack/theme selector. Select **Liquid Glass Icons**, if Smart Launcher recognizes the installed pack. Specific icon replacement requires a launcher that supports the app-filter format and matches the installed activity component names. Some icons may remain unchanged because only 117 activity mappings are predefined. You can use **Glassify My Installed Apps** to export extra transparent PNGs, then assign them to individual apps where your launcher supports custom icons.

## Build from source — no uploads required

All project code and vector artwork are already in the repository under these source bundles:

- `source/liquidglass-compact-v2.b64`: ZIP bundle of Gradle build scripts, Java activities, Android manifest, icon catalog, launcher mapping XML, and **639 SVGs** (637 themed icons plus pack branding/templates)
- `source/glass-overlays.b64`: original glass-overlay PNGs used for iconback/iconupon and fallback art
- `.github/workflows/build-apk.yml`: rebuilds Android source from the verified bundles, converts SVGs into 256×256 PNGs, validates the resources, and compiles the APK using Java 17, Android SDK 35, AGP 8.7.3, and Gradle 8.10.2

Both bundles are verified with SHA-256 in the workflow before being used.

To rebuild, select **Actions → Build Android APK → Run workflow**.

## Notes

- The gallery is offline and does not require a user account.
- The installed-app glassifier uses a copy of the phone's own launchable app icon, adds the ultra-glossy glass styling, and saves an exportable transparent PNG.
- Full automatic support for every app or every stock Android launcher is not possible through an ordinary icon pack; support varies by launcher and installed app versions.
- Some glyphs are simplified artistic interpretations for visual consistency.

Source project license: see LICENSE inside the bundled source.
