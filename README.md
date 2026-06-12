# 🩺 Medical Inventory Pro - Flutter Mobile App

A complete, production-ready Flutter mobile application for medical inventory management with role-based access, stock tracking, and order management.

## ✨ Features

- 🔐 **Secure Authentication** - JWT-based login system
- 👥 **Role-Based Access** - Separate interfaces for Admin and Doctor
- 💊 **Inventory Management** - Add, track, and manage medicines
- 📋 **Order System** - Place, approve, and track orders
- 💰 **Commission Tracking** - Automatic commission calculations
- 📱 **Mobile-First Design** - Beautiful Material Design UI
- 🔄 **Real-Time Updates** - Live stock and order status
- 🌐 **API Integration** - Connects to backend server

## 🎯 Demo Credentials

| Role | Username | Password |
|------|----------|----------|
| **Admin/MR** | `admin` | `admin123` |
| **Doctor** | `dr_sharma` | `doc123` |

## 📦 What's Included

- ✅ Complete Flutter source code
- ✅ API service for backend communication
- ✅ Authentication screens
- ✅ Admin dashboard with stock management
- ✅ Doctor dashboard with order placement
- ✅ Data models and services
- ✅ Error handling and loading states
- ✅ Responsive UI for all screen sizes

## 🚀 Quick Start

### Prerequisites
- Flutter SDK 3.0+
- Android Studio or Xcode
- Physical device or emulator

### Installation

1. **Navigate to project directory**
   ```bash
   cd medical-inventory-flutter
   ```

2. **Get dependencies**
   ```bash
   flutter pub get
   ```

3. **Run on device/emulator**
   ```bash
   flutter run
   ```

## 📱 Building APK

### Debug Build (for testing)
```bash
flutter build apk --debug
```

### Release Build (for distribution)
```bash
flutter build apk --release
```

**Output location:** `build/app/outputs/flutter-apk/app-release.apk`

See `BUILD_GUIDE.md` for detailed instructions.

## 🏗️ Project Structure

```
lib/
├── main.dart                    # App entry point
├── models/                      # Data models
│   ├── user.dart               # User model
│   ├── medicine.dart           # Medicine model
│   └── order.dart              # Order model
├── services/
│   └── api_service.dart        # Backend API communication
└── screens/
    ├── login_screen.dart       # Login interface
    ├── doctor_dashboard.dart   # Doctor interface
    └── admin_dashboard.dart    # Admin interface
```

## 🔌 API Integration

The app connects to the backend API at:
```
https://5000-i3a7ryqoy466nk98ngf1r-99c534a0.sg1.manus.computer/api
```

### API Endpoints Used
- `POST /auth/login` - User authentication
- `GET /medicines` - Get all medicines
- `POST /medicines` - Add new medicine (Admin only)
- `GET /orders` - Get user's orders
- `POST /orders` - Place new order (Doctor only)
- `PUT /orders/:id/status` - Update order status (Admin only)
- `GET /stats` - Get dashboard statistics (Admin only)

## 🎨 UI Components

- **Login Screen** - Email/password authentication
- **Doctor Dashboard** - Browse medicines and place orders
- **Admin Dashboard** - Manage inventory and approve orders
- **Order Cards** - Display order details with status
- **Medicine Cards** - Show medicine details with order form

## 🔐 Security Features

- JWT token-based authentication
- Secure token storage using SharedPreferences
- HTTPS communication
- Input validation
- Error handling

## 📊 Database Models

### User
- id, username, role (admin/doctor)

### Medicine
- id, name, company, stock, price, expiry_date, commission_pct, scheme

### Order
- id, doctor_name, med_name, qty, total_bill, mr_commission, order_date, status

## 🐛 Troubleshooting

### Build Issues
```bash
flutter clean
flutter pub get
flutter build apk --release
```

### Connection Issues
- Ensure backend server is running
- Check internet connection
- Verify API URL in `lib/services/api_service.dart`

### Device Issues
```bash
# List connected devices
flutter devices

# Run on specific device
flutter run -d <device_id>
```

## 📚 Dependencies

- `http` - HTTP client for API calls
- `shared_preferences` - Local data storage
- `provider` - State management
- `intl` - Internationalization

## 🚀 Deployment

### Google Play Store
1. Create Google Play Developer account
2. Sign APK with release key
3. Upload to Play Store
4. App becomes available to users

### Direct Distribution
1. Host APK on server
2. Share download link
3. Users install directly

### Firebase App Distribution
1. Upload to Firebase Console
2. Share link with testers
3. Auto-updates available

## 📝 Build Commands Reference

```bash
# Development
flutter run                          # Run on device
flutter run -d emulator             # Run on emulator

# Building
flutter build apk --debug           # Debug APK
flutter build apk --release         # Release APK
flutter build appbundle --release   # App Bundle (Play Store)

# Maintenance
flutter clean                       # Clean build artifacts
flutter pub get                     # Get dependencies
flutter pub upgrade                 # Upgrade dependencies
flutter doctor                      # Check environment
```

## 🎯 Features by Role

### Doctor
- ✅ View available medicines
- ✅ Place orders
- ✅ Track order status
- ✅ View order history

### Admin/MR
- ✅ Add new medicines
- ✅ Manage inventory
- ✅ View all orders
- ✅ Approve/reject orders
- ✅ View sales statistics
- ✅ Track commissions

## 📞 Support

For issues or questions:
1. Check `BUILD_GUIDE.md` for build-related help
2. Run `flutter doctor` to verify environment
3. Check backend server status
4. Verify internet connection

## 📄 License

MIT License - Feel free to use and modify

---

**Built with ❤️ using Flutter**

For detailed build instructions, see `BUILD_GUIDE.md`
