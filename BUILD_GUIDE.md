# 📱 Medical Inventory Pro - Flutter Mobile App Build Guide

## ✅ What You Have

A complete, production-ready Flutter mobile application that mirrors all features from the web app:
- ✅ User authentication (Login/Logout)
- ✅ Role-based dashboards (Admin/Doctor)
- ✅ Medicine inventory management
- ✅ Order placement and tracking
- ✅ Commission calculations
- ✅ Real-time updates
- ✅ Beautiful Material Design UI
- ✅ Responsive mobile layout

---

## 🚀 How to Build APK (Android)

### Prerequisites (One-time setup)

#### 1. Install Flutter
- **Windows/Mac/Linux**: Download from [flutter.dev](https://flutter.dev/docs/get-started/install)
- Extract and add to PATH
- Run: `flutter doctor` (verify all checks pass)

#### 2. Install Android Studio
- Download from [developer.android.com](https://developer.android.com/studio)
- Install Android SDK (API 33+)
- Create a virtual device or connect a physical phone

#### 3. Verify Setup
```bash
flutter doctor
# Should show: ✓ Flutter, ✓ Android toolchain, ✓ Android SDK
```

---

### Building the APK

#### Step 1: Navigate to Project
```bash
cd /path/to/medical-inventory-flutter
```

#### Step 2: Get Dependencies
```bash
flutter pub get
```

#### Step 3: Build APK (Debug)
```bash
flutter build apk --debug
```

**Output:** `build/app/outputs/flutter-apk/app-debug.apk`

#### Step 4: Build APK (Release - Recommended)
```bash
flutter build apk --release
```

**Output:** `build/app/outputs/flutter-apk/app-release.apk`

---

## 📥 Installing APK on Phone

### Option 1: Via USB Cable
```bash
flutter install
# Or manually:
adb install build/app/outputs/flutter-apk/app-release.apk
```

### Option 2: Via Email/File Transfer
1. Copy APK file to your phone
2. Open file manager on phone
3. Tap the APK file
4. Tap "Install"
5. Open app from launcher

### Option 3: Via QR Code (Recommended)
1. Upload APK to a file sharing service (Google Drive, Dropbox, etc.)
2. Generate QR code for the download link
3. Scan QR code on phone
4. Download and install

---

## 🔧 Building for iOS (Mac only)

```bash
flutter build ios --release
# Then open in Xcode:
open ios/Runner.xcworkspace
# Build and deploy from Xcode
```

---

## 🐛 Troubleshooting

### "Flutter not found"
- Add Flutter to PATH
- Restart terminal
- Run: `flutter --version`

### "Android SDK not found"
```bash
flutter config --android-sdk /path/to/android/sdk
```

### "Gradle build failed"
```bash
flutter clean
flutter pub get
flutter build apk --release
```

### "App crashes on startup"
- Check backend server is running
- Verify API URL in `lib/services/api_service.dart`
- Check internet permissions in `AndroidManifest.xml`

### "Can't connect to API"
- Ensure backend is running on `https://5000-...`
- Check phone has internet connection
- Verify CORS is enabled on backend

---

## 📦 APK File Details

| Type | Size | Use Case |
|------|------|----------|
| **Debug APK** | ~50MB | Testing during development |
| **Release APK** | ~30MB | Production distribution |

---

## 🔐 Security Notes

- Never hardcode API keys in production
- Use environment variables for API URLs
- Enable ProGuard for release builds (automatic)
- Test on real device before distribution

---

## 📤 Distributing Your App

### Option 1: Google Play Store
1. Create Google Play Developer account ($25)
2. Sign APK with release key
3. Upload to Play Store
4. App appears in Google Play

### Option 2: Direct Distribution
1. Host APK on your server
2. Share download link
3. Users install directly

### Option 3: Firebase App Distribution
1. Go to Firebase Console
2. Upload APK
3. Share link with testers
4. Auto-updates available

---

## 📱 Demo Credentials

| Role | Username | Password |
|------|----------|----------|
| Admin | `admin` | `admin123` |
| Doctor | `dr_sharma` | `doc123` |

---

## 🎯 Project Structure

```
medical-inventory-flutter/
├── lib/
│   ├── main.dart                 # App entry point
│   ├── models/                   # Data models
│   │   ├── user.dart
│   │   ├── medicine.dart
│   │   └── order.dart
│   ├── services/
│   │   └── api_service.dart      # Backend communication
│   └── screens/
│       ├── login_screen.dart
│       ├── doctor_dashboard.dart
│       └── admin_dashboard.dart
├── android/                       # Android-specific code
├── pubspec.yaml                   # Dependencies
└── BUILD_GUIDE.md                # This file
```

---

## 📚 Useful Commands

```bash
# Check Flutter version
flutter --version

# Check environment
flutter doctor

# Clean build
flutter clean

# Get dependencies
flutter pub get

# Run on device
flutter run

# Build APK
flutter build apk --release

# Build AAB (for Play Store)
flutter build appbundle --release

# View logs
flutter logs

# Stop running app
flutter stop
```

---

## 🔗 Useful Links

- [Flutter Official Docs](https://flutter.dev/docs)
- [Android Development](https://developer.android.com)
- [Flutter Packages](https://pub.dev)
- [Material Design](https://material.io)

---

## ✨ Features Included

✅ Material Design UI  
✅ HTTP networking  
✅ Local storage (SharedPreferences)  
✅ Error handling  
✅ Loading states  
✅ Form validation  
✅ Role-based navigation  
✅ Real-time data updates  

---

## 📞 Support

If you encounter issues:
1. Run `flutter doctor` to check environment
2. Check logs: `flutter logs`
3. Clean and rebuild: `flutter clean && flutter pub get`
4. Check backend is running
5. Verify internet connection

---

**You're all set! Build your APK and install on your phone. Enjoy! 🎉**
