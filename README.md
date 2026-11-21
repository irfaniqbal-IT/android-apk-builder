# android-apk-builder

[![Build APK](https://github.com/irfaniqbal-IT/android-apk-builder/actions/workflows/build-apk.yml/badge.svg)](https://github.com/irfaniqbal-IT/android-apk-builder/actions/workflows/build-apk.yml)

Push an Android Studio project here and GitHub Actions builds the APK automatically.

## ✅ Requirements
- An Android Studio project (Kotlin or Java) with the **Gradle wrapper** (`gradlew`, `gradle/wrapper/`)
- App module named `app` (default in Android Studio)
- JDK 17 compatible build (Android Gradle Plugin 8.x)

## 🚀 How to use
1. Create a project in Android Studio.
2. Copy the project files into this repo's root (keep `.github/`, `.gitignore`, `README.md`, `LICENSE`).
3. Push to `main`:
   ```bash
   git clone https://github.com/irfaniqbal-IT/android-apk-builder.git
   cd android-apk-builder
   # copy your Android project files here
   git add .
   git commit -m "Add Android project"
   git push
   ```
4. Open the **Actions** tab → latest **Build APK** run → download **app-debug-apk** from *Artifacts*.

You can also run the build manually: **Actions → Build APK → Run workflow**.

## 📦 Expected structure
```
android-apk-builder/
├── .github/workflows/build-apk.yml
├── app/
│   ├── build.gradle(.kts)
│   └── src/main/
├── gradle/wrapper/
├── build.gradle(.kts)
├── settings.gradle(.kts)
├── gradlew
└── gradlew.bat
```

## 🔐 Release (signed) APK — later
Store your keystore as GitHub **Secrets** (Settings → Secrets and variables → Actions), never in the repo.

## 📄 License
MIT
