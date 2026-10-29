# Golan Cleaner Pro

[Feature and use guide](GUIDE.md) · [دليل الاستخدام العربي](GUIDE.ar.md) · [Releases: APK and complete source](https://github.com/GOLAN2CODE/golan-cleaner-pro/releases)

[العربية](README.ar.md)

Android storage/file-management preview **0.11.1 / code 14**, package `app.golan.cleaner.pro`; Android 9/API 28 minimum, SDK/target 36. Arabic/English, RTL/LTR and system light/dark support with the GOLAN broom identity. The delivered APK is debug-signed.

## Features

- **Clean:** scoped storage analysis, reviewed suggestions, bounded private recovery and explicitly enabled automatic cleanup.
- **Files:** accessible folder browsing, current-folder search/sort, selection, open/share/details, new folder, rename, file copy/move and reviewed removal where the current backend and grants allow it.
- **Saved:** opt-in future notification text and available images for explicitly selected conversations, encrypted private storage and permission/media diagnostics.
- Device information, visible-app permission details, Android-confirmed app uninstall, manual cache-setting links, Settings and About.

## Install and access

Download the APK from release assets and verify `SHA256SUMS.txt`. Enable installation for its opening app and install. Grant Android storage/folder access manually only for the areas you want to use. Android 9 uses storage permissions, Android 10 may require a folder grant, and Android 11+ optionally uses all-files access. Broad access alone does not enable automatic cleanup. Notification archiving has a separate disclosure, manual notification-access grant and conversation/text/image selection.

Updating requires a compatible existing signing key. Uninstalling or clearing app data destroys private recovery copies and notification archives. Keep important files elsewhere; do not treat the private recovery store as an independent backup.

## Full source and build

Download `golan-cleaner-pro-0.11.1-source.zip` from release assets and **extract it before building**. This ZIP contains complete sanitized `app` and `core` code, existing tests, resources and Gradle wrapper. A README-only repository view is not the full source.

Install a JDK 17 Gradle host, JDK 21 toolchain, Android SDK 36 and compatible build tools. Configure SDK and Java discovery locally, or create your own untracked `local.properties` with `sdk.dir`. From the extracted root:

```powershell
.\gradlew.bat :app:assembleDebug
```

Linux/macOS: `chmod +x gradlew && ./gradlew :app:assembleDebug`. Normal output: `app/build/outputs/apk/debug/app-debug.apk`. Gradle/Maven downloads need network access. A locally built debug key can differ from the delivered APK. Existing tests are retained; no new build, test run or phone operation was performed during packaging.

## Practical limits

Automatic cleanup is OFF by default. It needs an explicit policy for up to eight exact folders, approved old temporary/cache contents, a minimum age of 14 days, two unchanged observations at least 30 seconds apart, and fresh access/identity checks. Per-run limits are 20 files/16 MiB with a cooperative 60-second budget; blocked storage I/O does not have a guaranteed hard deadline. Daily jobs are optional and inexact.

Reviewed removal first creates a verified private recovery copy and journal. File removal is bounded to 100 files and 256 MiB per file; shared recovery capacity is 1 GiB with a 16 MiB reserve and no automatic purge. Restore uses a fresh name. Copies consume storage until manually removed; backup bytes are not automatically freed-space savings. Folder listings are bounded to 2,000 direct entries and identify incomplete results. No recursive folder mutation/overwrite or unrestricted access to app-private/system/Android-data areas is promised.

Notification capture covers future eligible selected conversations only. Supported JPEG/PNG/WebP images need an offered URI and current read grant; an image may be a thumbnail. Image capture is bounded to 8 MiB per item and 128 MiB total private blob reservations. **Video acquisition/downloading is not implemented.** The MP4/video counters are capability diagnostics, not saved-video functionality. This app cannot prevent sender deletion or recover old unseen messages. It has no Internet permission, root or Accessibility cleaning service.

The existing 0.11.1 checkpoint records 729 tests/71 suites, zero failures and zero lint errors with 51 warnings, and bounded Motorola install/launch checks. Those are prior results; actual social-app image/video acceptance, all devices and every file operation are not established. Motorola shared-storage/automatic folder setup remains grant-dependent.

## Snapshot and licensing

Personal logs, device identifiers, screenshots, backups, build caches, private evidence and historical instructions are excluded. Application code and tests remain unchanged. No project-wide license was present or added. Dependency license material is preserved in `LICENSES/`; see [THIRD_PARTY.md](THIRD_PARTY.md) and [LICENSE-STATUS.md](LICENSE-STATUS.md).
