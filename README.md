# Black Screen App

A lightweight Android app that displays a pure black screen while you use other apps in Picture-in-Picture (PiP) mode. The Black Screen App acts as a full-screen black background, and PiP windows from other apps appear on top of it. Designed to save battery and reduce power consumption on OLED/AMOLED screens without turning off the display.

## Why Use This App?

When you're watching videos or using apps in Picture-in-Picture mode, the screen stays on and consumes power. This app displays a full-screen pure black background behind your PiP content. Because OLED/AMOLED pixels are completely off when displaying black, power consumption drops significantly while keeping your device awake and the screen on.

## Features

- **PiP-compatible black background** — displays a pure black screen while you use other apps in Picture-in-Picture mode
- **Battery saving** — pure black (`#000000`) minimizes power consumption on OLED/AMOLED screens
- **Keeps the screen awake** — prevents auto-lock while the overlay is active
- **Hides status bar and navigation bar** — full immersion for a true black screen experience
- **Automatically re-applies settings** — restores black screen when returning to the app
- **Portrait orientation** — consistent experience across devices

## How It Works

1. Start using an app in Picture-in-Picture mode (e.g., YouTube, video player)
2. Open the Black Screen App
3. The Black Screen App displays a full-screen pure black background
4. Your PiP content appears on top of the black screen
5. Because OLED/AMOLED pixels are completely off when displaying black, power consumption drops significantly
6. Continue using your device normally — the black background stays visible and the screen stays awake

## Installation

### Android APK

Download the release APK and install it directly on your Android device:

1. Download [`black-screen-app.apk`](https://drive.google.com/file/d/16ExR6btUis2PtJjfowYEN4IaaLf8YmQ1/view?usp=sharing)
2. Transfer the APK to your Android device
3. Enable installation from unknown sources (Settings > Security > Unknown Sources)
4. Open the APK file and follow the installation prompts

> **Note:** This is a release build. It may show a warning about being from an unknown source, which is expected for apps installed outside of the Google Play Store.

### Building the Release APK

To build the release APK yourself:

```bash
./gradlew assembleRelease
```

The release APK will be generated at `app/build/outputs/apk/release/app-release.apk`.

## Usage

1. Start a video or media app and enter Picture-in-Picture mode
2. Open the Black Screen App
3. The app displays a full-screen black background
4. Your PiP content appears on top of the black background, helping save battery
5. Use your device normally
6. To exit, open the Black Screen App again and close it

## Development

### Prerequisites

- Android Studio
- JDK 11
- Android SDK with compileSdk 36

### Get started

1. Open the project in Android Studio
2. Sync Gradle dependencies
3. Run on an Android device or emulator

## Tech Stack

- **Language:** Kotlin
- **UI:** Jetpack Compose
- **Build System:** Gradle (AGP 9.2.1)
- **Min SDK:** 26
- **Target SDK:** 36

## Project Structure

```
app/
  src/
    main/
      java/com/devijem/blackscreenapp/
        MainActivity.kt          # Main activity with immersive mode
        ui/theme/
          Theme.kt               # Compose theme
          Color.kt               # Color definitions
          Type.kt                # Typography definitions
      res/
        layout/
          activity_main.xml      # Black screen layout
        values/
          strings.xml
          colors.xml
          themes.xml
        drawable/                # App icons and drawables
        mipmap-*/                # Launcher icons
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
