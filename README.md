# RRB Group D Current Affairs Quiz — Android project

This project wraps the supplied HTML quiz in an Android WebView. The HTML quiz is copied unchanged into `app/src/main/assets/index.html`.

## Build an APK with GitHub + Codemagic

1. Extract this ZIP.
2. Create a new **public or private GitHub repository**.
3. Upload/push all files and folders from this project to the repository root (the `codemagic.yaml` file must be at the root).
4. In Codemagic, connect GitHub and select this repository.
5. Start a build using the `Android APK` workflow.
6. When the build completes, download the APK from the build artifacts.

Codemagic workflow artifact:
`app/build/outputs/apk/release/app-release-unsigned.apk`

This is an **unsigned release APK**. It can be used for testing/sideloading on many Android devices, but Google Play publishing requires signing. Configure Android code signing in Codemagic before publishing.

## Build locally (optional)

Install Android Studio and a compatible JDK/Android SDK, open this project, then build the `app` module. Alternatively, run `gradle assembleRelease` from the project root if Gradle and the Android SDK are configured.

## App behavior

- Loads the quiz locally; no website hosting is required.
- JavaScript and DOM storage are enabled so the HTML quiz can use its existing quiz logic and `localStorage`.
- Quiz content, colors, saved/wrong-question behavior, and existing controls are preserved from the supplied HTML file.
- The HTML content itself has not been edited as part of Android packaging.
