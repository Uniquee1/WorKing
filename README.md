# WorKing

WorKing is an offline-first Android app for keeping employment details, attendance, calendar events, leave and benefit balances, and an estimated pay view together on your phone. The Android app bundles its interface locally; records are stored in this app's local browser storage on the device.

## Build the Android APK

Requirements: Android SDK platform 37 and matching Android build tools, plus JDK 17 or newer.

1. Set `ANDROID_HOME` to your Android SDK location, or put the SDK path in `local.properties` as `sdk.dir=...`.
2. From this folder run `gradlew.bat assembleDebug` on Windows, or `./gradlew assembleDebug` on macOS/Linux.
3. Install `app/build/outputs/apk/debug/app-debug.apk` on an Android device. The debug APK is signed for local installation.

## MVP notes

- Home, calendar, benefits and profile sections with editable local records.
- Attendance is entered by the user; missing past entries remain unconfirmed.
- Weekly schedules classify workdays and rest days. 2026 national holidays are prefilled and editable.
- Pay and holiday/overtime calculations are estimates using the user's configurable rates.
- This MVP does not connect to an employer, sync to the cloud, or provide payroll or tax advice.
