# 🎬 CineWave - Movie Discovery Application

## 📋 Project Overview
CineWave is a Flutter mobile application for discovering movies, managing favorites, and creating watchlists. The app fetches real-time movie data from The Movie Database (TMDB) API and provides a beautiful, responsive user interface.

## 🚀 Setup Instructions

### Prerequisites
Ensure you have the following installed:
- **Flutter SDK** (version 3.19.0 or higher)
- **Dart** (version 3.0.0 or higher)
- **Android Studio** or **VS Code** with Flutter extension
- **Android Emulator** or **Physical Android Device**

### Installation Steps

1. **Clone/Download the Project**
   ```bash
   # Clone the repository
   git clone <repository-url>
   cd cinewave
Or simply download and extract the ZIP file.

Install Dependencies

bash
flutter pub get
Configure API Key

The app comes with a demo TMDB API key

For production, get your own free key from: https://www.themoviedb.org/settings/api

Replace in code: 9bb89316d8693b06d7a84980b29c011f with your key

Verify Setup

bash
flutter doctor
Ensure all checks pass (especially for Android/iOS toolchain).

📱 Steps to Run Locally
For Android
bash
# Connect your device/emulator
flutter devices

# Run the application
flutter run
For iOS (macOS only)
bash
flutter run -d ios
For Web
bash
flutter run -d chrome
Build APK
bash
# Debug APK
flutter build apk --debug

# Release APK
flutter build apk --release
🛠 Dependencies Used
Core Dependencies (pubspec.yaml)
yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^1.1.0      # For API calls to TMDB
  intl: ^0.19.0     # For date formatting
  shimmer: ^3.0.0   # For loading animations
API Dependencies
TMDB API: Free movie database (https://www.themoviedb.org/)

API Endpoint: https://api.themoviedb.org/3/movie/popular

Image CDN: https://image.tmdb.org/t/p/w500

Platform Dependencies
Android: minSdkVersion 21

iOS: iOS 11.0+ (if building for iOS)

Internet Permission: Required for API calls

⚙️ Assumptions Made
1. API Limitations
Using free TMDB API tier (rate-limited)

Demo API key provided for testing

Images may be subject to TMDB terms of use

2. User Experience
No user authentication required (as per requirements)

Favorites/Watchlist stored locally in app state (not persisted)

Internet connection required for initial movie loading

3. Development Assumptions
Single-file architecture (all code in main.dart as requested)

Material Design guidelines followed

Responsive for common phone sizes (360x640 to 414x896)

Blue and white color theme as specified

4. State Management
Basic setState() used for simplicity

No external state management libraries

Loading, error, and empty states implemented

