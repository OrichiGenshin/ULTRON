# ULTRON Android Assistant (v1.0)

A clean native Kotlin starter for Android 6.0+ (tested target: Android 11 / API 30; compile SDK 35).

## Current features
- Tap-to-activate speech recognition using Android's speech service
- British English system text-to-speech voice where available
- Open installed apps by their exact launcher label
- Open Android Settings
- Search the web
- Open the messaging app for a user-reviewed message

## Important limitations
- This starter does not run a background hotword listener.
- It does not identify or authenticate a speaker by voice.
- It does not silently send SMS or messages. Messaging is opened so the user can choose a recipient and review/send.
- Speech recognition availability and voice quality depend on services installed on the phone.
- Android may require the user to grant microphone permission.

## Build APK with GitHub Actions
1. Upload the contents of this folder to the root of a GitHub repository (not the ZIP file nested inside another folder).
2. Keep the `.github/workflows/android.yml` file in that exact path.
3. Open the repository's **Actions** tab.
4. Run **Build ULTRON APK** (or push to `main`).
5. Open the completed workflow run and download the `ULTRON-debug-apk` artifact.
6. Extract the artifact ZIP and install `app-debug.apk` on the phone. Allow installation from that source if Android asks.

## Technical setup
- Android Gradle Plugin: 8.7.3
- Gradle: 8.9 (provided by GitHub Actions; no wrapper ZIP is extracted)
- Kotlin Android plugin: 2.0.21
- Java: 17
- compileSdk: 35
- minSdk: 23
- targetSdk: 35

The workflow checks out and builds the actual repository source directly. It does not extract an old starter ZIP.
