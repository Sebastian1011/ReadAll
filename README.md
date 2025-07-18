# ReadAll

This project is a minimal Android application built with Kotlin and Gradle.

## Development setup

1. Install JDK 21 or later.
2. Install the Android SDK. Configure the SDK location via the `ANDROID_HOME` environment variable or by creating a `local.properties` file in the project root containing:
   ```
   sdk.dir=/path/to/android/sdk
   ```

## Building the APK

### Debug build

Run the following command to generate a debug APK:

```bash
./gradlew assembleDebug
```

The resulting file will be located at `app/build/outputs/apk/debug/app-debug.apk`.

### Release build

To build a release APK run:

```bash
./gradlew assembleRelease
```

The release artifact can be found at `app/build/outputs/apk/release/app-release.apk`.

### Testing

Execute unit tests with:

```bash
./gradlew test
```

## CI/CD pipeline

GitHub Actions automatically builds the release APK whenever code is pushed to the `main` branch. The workflow defined in `.github/workflows/android.yml` installs the Android SDK, builds the release variant and uploads the APK as both a workflow artifact and a GitHub release asset.

The generated APK can be downloaded from the workflow run artifacts or the repository's Releases page.
