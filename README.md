# Byblos Car Rental Platform

A native Android application that streamlines the car-rental experience for customers and branch staff, providing booking management, branch configuration, and analytics-ready telemetry through Firebase services.

## Features
- Customer onboarding with mobile-friendly forms and input validation
- Branch configuration for services, pricing, and availability windows
- Vehicle catalogue browsing with filtered search and booking creation
- Real-time booking persistence backed by Firebase Realtime Database
- Analytics hooks ready via Firebase Analytics
- ViewBinding-enabled UI for safer, faster layout access

## Tech Stack
- **Frontend / Mobile:** Android, Kotlin, Java, ViewBinding, AndroidX Navigation
- **Backend / Cloud:** Firebase Realtime Database, Firebase Analytics
- **Build & Tooling:** Gradle 7.x, Android Studio Arctic Fox or newer, Kotlin plugin, Google Services plugin

## Project Structure
- `app/` – Android application module (add your code under `app/src/main/...`)
- `app/google-services.example.json` – Placeholder Firebase configuration; copy your real file as `google-services.json` (kept out of version control)
- `src/` – Reserved for shared source/assets if you split modules later
- `docs/` – Space for architecture diagrams and UI screenshots
- `build.gradle`, `settings.gradle`, `gradle.properties` – Root Gradle configuration
- `LICENSE` – MIT license for the repository

## How to Run
1. **Requirements:** Android Studio (Arctic Fox or newer), JDK 11+, Android SDK 31, and a configured Android device/emulator.
2. **Clone:** `git clone <repo-url> && cd Byblos`
3. **Firebase config:** Download your Firebase `google-services.json` from the console and place it at `app/google-services.json` (the sample file shows the expected shape).
4. **Gradle wrapper:** If `gradle/wrapper` is missing after clone, run `gradle wrapper --gradle-version 7.0.2` once (requires local Gradle) so `./gradlew` works.
5. **Sync & build:** Open the project in Android Studio, let it sync dependencies, then run `./gradlew assembleDebug` or press Run to launch on a device/emulator.

## What This Project Demonstrates
- Mobile architecture setup with Gradle-based modularization and ViewBinding
- Cloud-backed data flows using Firebase services
- Dependency management and environment isolation via Google Services plugin and build variants
- Test-ready configuration with JUnit, Truth, Espresso, and Mockito dependencies declared

## Future Improvements
- Add full CI pipeline (GitHub Actions) for linting, unit, and instrumentation tests
- Implement offline caching and conflict resolution for bookings
- Harden authentication/authorization with Firebase Auth and role-based rules
- Expand UI state management (e.g., ViewModel + LiveData/Flow) and error handling
- Add automated screenshot generation for release documentation

## Author
Omar Khattab
