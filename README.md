# Liquid Glass Icons — v2.0 Ultra Gloss

A **native Android icon-pack app** featuring 637 ultra-glossy, translucent icons, a searchable gallery, 14 categories, 117 explicit launcher component mappings, and a built-in **Glassify My Installed Apps** tool for apps outside the predefined set.

## Download the Android APK

1. Open the [GitHub Actions build page](https://github.com/Wayudiesa24/LiquidGlassIcons/actions/workflows/build-apk.yml).
2. Open the most recent successful **Build Android APK** run.
3. Under **Artifacts**, download `LiquidGlassIcons-v2.0.1-SmartLauncher-APK`.
4. Extract the artifact ZIP and install `app-debug.apk` on your Android phone.

This is an Android **debug-signed APK** for personal testing, not a Play Store release. Android 8.0 or later is required.

## Apply with Smart Launcher 6 (v2.0.1 fix)

**The v2.0.0 APK omitted Smart Launcher's required `ginlemon.smartlauncher.THEMES` discovery intent**, so Smart Launcher 6 could not find it even though the app gallery could open. v2.0.1 declares the required Smart Launcher action, ADW theme aliases, and Nova icon-pack actions; GitHub Actions verifies the final APK contains the Smart Launcher discovery action.

1. Install the latest **v2.0.1** APK.
2. Open **Smart Launcher → Settings → Global appearance → Icon appearance → Icon pack** (settings labels may vary).
3. Select **Liquid Glass Icons** from the installed packs.
4. If the pack does not appear immediately, close and reopen Smart Launcher. Do **not** clear Smart Launcher's storage/data (which could reset your layout).

**Debug APK update caveat:** The GitHub hosted builder signs each run with its own debug key. If Android says an update cannot be installed, uninstall the **older Liquid Glass Icons** app first, then install v2.0.1. This affects only the icon pack app, not Smart Launcher. The app is local-first, but uninstalling could remove internal app settings; export any manually glassified PNGs before uninstalling.

Automatic replacement still depends on supported activity mappings. The gallery includes 637 designs; only 117 explicit activity mappings are defined. For unrecognized installed apps, use Glassify My Installed Apps and assign exported PNGs manually where Smart Launcher supports it.

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
