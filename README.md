# FitAI

An AI fitness companion — personalized workout and nutrition plans with health tracking, built with Flutter and Firebase.

## Features

- **Onboarding** — personal info, fitness goals, workout preferences, and nutrition/health intake, ending in a summary profile
- **Workouts** — plan setup, exercise catalog, guided workout screens, session logging, exercise logs, and a workout calendar
- **Nutrition** — nutrition plans and daily tracking
- **Health dashboard & progress** — health data, progress screens, and profile management
- **AI chat** — an in-app AI chat for fitness and nutrition questions

## Tech

- Flutter / Dart (Android, iOS, web, and desktop targets)
- Firebase — Auth, Firestore (see `firestore.rules` and `firestore.indexes.json`), and Cloud Functions (`functions/`)

## Run it

```bash
flutter pub get
flutter run
```

This app expects a Firebase project. After creating one:

1. **Android:** add an app with package name `com.jeeva.fitai`, then download `google-services.json` into `android/app/`
2. **iOS:** add an app with bundle ID `com.jeeva.fitai`, then download `GoogleService-Info.plist` into `ios/Runner/`
3. Or regenerate the config with `dart run flutterfire configure`

## Structure

```
lib/
  models/     user profile, workout/nutrition plans, health data, logs
  providers/  user, workout, nutrition, chat, theme state
  screens/    onboarding, home, workout, nutrition, health, progress, chat, profile
  services/   app services (including the AI agent service)
functions/    Firebase Cloud Functions
```
