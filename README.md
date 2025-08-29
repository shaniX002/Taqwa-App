# 🌙 Taqwa – Islamic Mobile App

Taqwa is a complete **Islamic lifestyle app** built with **Flutter**, designed to support Muslims in their daily religious and spiritual activities. It combines the **Holy Quran, Duas, Prayer utilities, Learning/Teacher section, Notifications, and Islamic resources** in one mobile application.

The app integrates **modern UI/UX** with Flutter frontend and a **Firebase-powered backend** for analytics, crash reporting, push notifications, and cloud features.

---

## 📋 Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Tech Stack](#tech-stack)
* [Screenshots](#screenshots)
* [App Structure](#app-structure)
* [Installation](#installation)
* [Firebase Setup](#firebase-setup)
* [Localization](#localization)
* [Permissions](#permissions)
* [Build & Release](#build--release)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)

---

## 📖 Overview

Taqwa is not just a Quran app, it’s a **daily Islamic assistant**. From Quran recitation to prayer utilities and Duas, it offers everything a Muslim needs on their phone. With built-in **localization**, it supports multiple languages like **English, Urdu, and Arabic**.

The goal is to provide a **simple, fast, and clean mobile experience** for Muslims worldwide.

---

## ✨ Features

### Quran

* Full Quran text with **translations**
* **Audio recitation** with background play
* Bookmark Ayahs & Surahs
* Night mode for easy reading

### Duas

* Collection of **daily Duas** (morning, evening, travel, etc)
* Category-based navigation
* Share Duas with friends via social apps

### Teacher / Learning Section

* **Islamic lectures or lessons**
* Notes and Q\&A area
* Resource library for continuous learning

### Prayer Utilities

* **Hijri calendar** integration
* **Qibla compass** using phone sensors
* Prayer time reminders & custom alarms
* Islamic events notifications

### Notifications

* Push notifications using **Firebase Cloud Messaging (FCM)**
* Daily reminders for Quran reading or prayer
* Smart alerts (Ramadan, Eid, Islamic events)

### Multimedia

* **Just Audio** for smooth playback
* Audio service for background audio
* Media controls on lockscreen

### Social & Sharing

* Share Quran Ayahs or Duas
* Capture and share screenshots (e.g., Dua images)

---

## 🛠 Tech Stack

**Frontend**: Flutter (Dart SDK >= 3.5.3 < 4.0.0)
**State Management**: Riverpod
**Routing**: GoRouter
**Dependency Injection**: GetIt
**Backend**: Firebase (Core, Analytics, Crashlytics, Messaging)
**Networking**: Dio
**Storage**: SharedPreferences, PathProvider
**Audio**: Just Audio, Audio Service, Audio Session, Wakelock Plus
**Localization**: Easy Localization, Slang
**UI Libraries**: Google Fonts, ScreenUtil, Shimmer, AutoSizeText, Percent Indicator

---

## 🖼 Screenshots

> (Add your app screenshots here)

* Home screen
* Quran reader
* Duas section
* Qibla compass
* Teacher/Learning

---

## 📂 App Structure

```
lib/
  core/                 # Main app, routing, dependency injection
  features/
    quran/              # Quran reading and audio
    duas/               # Daily Duas
    teacher/            # Teacher and learning section
    prayer/             # Qibla, Hijri calendar, reminders
  common/
    widgets/            # Shared components (buttons, loaders, cards)
    utils/              # Constants, helpers, extensions
  l10n/                 # Localization
assets/
  images/               # App images
  translations/         # Language files (en.json, ur.json, ar.json)
test/                   # Unit and widget tests
pubspec.yaml
```

---

## ⚙️ Installation

### Prerequisites

* Install **Flutter SDK (>=3.5.3)**
* Install **Dart SDK**
* Android Studio / VS Code with Flutter setup
* Firebase project access

### Steps

1. Clone the repository:

   ```bash
   git clone <repo_url>
   cd taqwa
   ```
2. Install dependencies:

   ```bash
   flutter pub get
   ```
3. Run code generation (for localization etc):

   ```bash
   dart run build_runner build --delete-conflicting-outputs
   ```
4. Run the app:

   ```bash
   flutter run
   ```

---

## 🔥 Firebase Setup

1. Create Firebase project in console
2. Add Android app → download `google-services.json` → put in `android/app/`
3. Add iOS app → download `GoogleService-Info.plist` → put in `ios/Runner/`
4. Enable Firebase services:

   * Analytics
   * Crashlytics
   * Cloud Messaging (for notifications)
5. Configure Android Gradle files with Google Services plugin
6. Configure iOS with CocoaPods

---

## 🌐 Localization

The app supports multiple languages with **easy\_localization** and **slang**.

Steps:

* Add translations inside `assets/translations/`
* Example: `en.json`, `ur.json`, `ar.json`
* Wrap the app with EasyLocalization:

  ```dart
  EasyLocalization(
    supportedLocales: [Locale('en'), Locale('ur'), Locale('ar')],
    path: 'assets/translations',
    fallbackLocale: Locale('en'),
    child: MyApp(),
  )
  ```

---

## 🔑 Permissions

* **Location**: For Qibla compass and prayer times
* **Notifications**: For Duas and reminders
* **Storage/Media**: For saving/sharing screenshots

Configure in:

* `AndroidManifest.xml` (Android)
* `Info.plist` (iOS)

---

## 🚀 Build & Release

* **Debug Run**:

  ```bash
  flutter run -d android
  ```
* **Release APK**:

  ```bash
  flutter build apk --release
  ```
* **AppBundle (Play Store)**:

  ```bash
  flutter build appbundle --release
  ```
* **iOS Release**:

  ```bash
  flutter build ios --release
  ```

---

## 🛣 Roadmap

* [ ] Add offline Quran support
* [ ] Dark/Light themes
* [ ] Downloadable Duas packs
* [ ] User accounts & cloud sync
* [ ] In-app donation support
* [ ] More languages

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit changes with clear messages
4. Submit a pull request

