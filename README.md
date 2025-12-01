# 🚗 Aldaman Works - Car Rental & Purchase App

<div align="center">

**A comprehensive Saudi Arabian mobile application for car rental and purchase services**

[![Flutter](https://img.shields.io/badge/Flutter-3.6.1-blue.svg)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-3.6.1-blue.svg)](https://dart.dev/)
[![License](https://img.shields.io/badge/License-Private-red.svg)]()

[Features](#-features) • [Architecture](#-architecture) • [Tech Stack](#-tech-stack) • [Getting Started](#-how-to-run-the-project) • [Structure](#-folder-structure)

</div>

---

## 📱 Project Overview

**Aldaman Works** is a full-featured mobile application developed for the Saudi Arabian market, providing seamless car rental and purchase services. The app enables users to browse available vehicles, make reservations, purchase cars with flexible payment options (cash or financing), manage bookings, and interact with multiple branches across the Kingdom.

### Key Highlights
- 🇸🇦 **Saudi-focused**: Built specifically for the Saudi Arabian market with Arabic language support
- 🚀 **Production-ready**: Version 1.0.10+50 deployed and actively maintained
- 🏗️ **Scalable Architecture**: Clean Architecture with feature-based modular design
- 🔒 **Secure**: Secure storage, token-based authentication, and encrypted communication
- 📱 **Cross-platform**: Supports both iOS and Android platforms

---

## 🛠️ Tech Stack

### Core Framework
- **Flutter** `3.6.1` - Cross-platform UI framework
- **Dart** `^3.6.1` - Programming language

### State Management
- **flutter_bloc** `^9.1.0` - BLoC pattern implementation
- **provider** `^6.1.5` - State management for dependency injection

### Networking & API
- **dio** `^5.8.0+1` - HTTP client for API calls
- **pretty_dio_logger** `^1.4.0` - API request/response logging
- **connectivity_plus** `^6.1.4` - Network connectivity checking

### Dependency Injection
- **get_it** `^7.7.0` - Service locator pattern

### Local Storage
- **flutter_secure_storage** `^9.2.4` - Secure token storage
- **shared_preferences** `^2.5.3` - Simple key-value storage

### Firebase Services
- **firebase_core** `^4.0.0` - Firebase initialization
- **firebase_messaging** `^16.0.0` - Push notifications
- **firebase_crashlytics** `^5.0.0` - Crash reporting
- **flutter_local_notifications** `^19.4.0` - Local notifications

### UI & Design
- **flutter_screenutil** `^5.9.3` - Responsive UI scaling
- **flutter_svg** `^2.1.0` - SVG image support
- **cached_network_image** `^3.3.1` - Image caching
- **shimmer** `^3.0.0` - Loading placeholders
- **liquid_swipe** `^3.1.0` - Smooth page transitions
- **go_router** `^15.1.2` - Declarative routing
- **circle_nav_bar** `^2.2.0` - Custom navigation bar

### Maps & Location
- **flutter_map** `^8.1.1` - Interactive maps
- **latlong2** `^0.9.1` - Geographic coordinates
- **geolocator** `^13.0.2` - Location services

### Utilities
- **intl** `^0.20.2` - Internationalization
- **intl_phone_field** `^3.2.0` - Phone number input
- **url_launcher** `^6.3.1` - External URL launching
- **webview_flutter** `^4.13.0` - In-app web views
- **image_picker** `^1.1.2` - Image selection
- **flutter_image_compress** `^2.4.0` - Image compression
- **share_plus** `^11.0.0` - Content sharing
- **permission_handler** `^12.0.0+1` - Runtime permissions
- **dropdown_search** `^6.0.2` - Searchable dropdowns
- **app_links** `^6.4.0` - Deep linking support
- **confetti** `^0.8.0` - Celebration animations
- **flutter_html** `^3.0.0` - HTML rendering

### Functional Programming
- **dartz** `^0.10.1` - Functional programming utilities (Either, Option)

### Development Tools
- **flutter_lints** `^5.0.0` - Linting rules

---

## 🏗️ Architecture

This project follows **Clean Architecture** principles combined with the **BLoC (Business Logic Component)** pattern for state management. The architecture is organized into distinct layers, promoting separation of concerns, testability, and maintainability.

### Architecture Layers

```
┌─────────────────────────────────────┐
│      Presentation Layer             │
│  (UI, BLoC/Cubits, Widgets)         │
└─────────────────────────────────────┘
                 ↕
┌─────────────────────────────────────┐
│        Domain Layer                 │
│  (Entities, Use Cases, Repository)  │
└─────────────────────────────────────┘
                 ↕
┌─────────────────────────────────────┐
│         Data Layer                  │
│  (Models, Data Sources, Repository) │
└─────────────────────────────────────┘
```

#### **Presentation Layer**
- **Pages/Screens**: User interface screens
- **Controllers/Cubits**: Business logic and state management using BLoC pattern
- **Widgets**: Reusable UI components

#### **Domain Layer**
- **Entities**: Business objects (pure Dart classes)
- **Use Cases**: Single responsibility business logic operations
- **Repository Interfaces**: Contracts for data operations

#### **Data Layer**
- **Models**: Data transfer objects with JSON serialization
- **Data Sources**: Remote (API) and Local (cache/storage) data sources
- **Repository Implementations**: Concrete implementations of domain repositories

### Key Patterns

- **Dependency Injection**: Using GetIt service locator
- **Repository Pattern**: Abstracts data sources from business logic
- **Use Case Pattern**: Encapsulates single business operations
- **BLoC Pattern**: Manages state and business logic separately from UI
- **Either Pattern**: Uses `dartz` for functional error handling (Success/Failure)

### Feature-Based Structure

Each feature follows the same architectural pattern:
```
features/
  ├── [feature_name]/
  │   ├── Data/
  │   │   ├── DataSources/
  │   │   ├── Models/
  │   │   └── Repositories/
  │   ├── Domain/
  │   │   ├── Entities/
  │   │   ├── Repositories/
  │   │   └── UseCases/
  │   └── Presentation/
  │       ├── Controllers/
  │       ├── Pages/
  │       └── Widgets/
```

---

## ✨ Features

### 🔐 Authentication & User Management
- User registration with phone verification
- Login/Logout functionality
- Password recovery with OTP verification
- Profile management and updates
- Secure token-based authentication
- Account deletion support

### 🚗 Car Rental
- Browse available rental cars with filtering
- Advanced filters (brand, model, type, price, fuel type, transmission, etc.)
- View detailed car specifications and images
- Calendar-based date selection for rentals
- Individual and company rental options
- Rental offers and promotions
- Branch selection for pickup/dropoff
- Price calculation with insurance options
- Booking confirmation and management

### 💰 Car Purchase
- Browse cars available for sale
- Detailed car specifications and images
- Purchase options (cash or financing)
- Individual and company purchase flows
- Branch selection
- Promo code support
- Order placement and tracking

### 📅 Booking Management
- View all bookings (rental and purchase)
- Booking status tracking
- Booking details and history
- Booking cancellation (where applicable)

### ⭐ Favorites
- Add/remove cars to favorites
- Separate favorite lists for rental and purchase cars
- Quick access to saved vehicles

### 🔔 Notifications
- Push notifications via Firebase Cloud Messaging
- Local notifications
- In-app notification center
- Notification history

### 🗺️ Location Services
- Branch location mapping
- Google Maps integration
- Location-based services

### 🌍 Localization
- Full Arabic language support
- RTL (Right-to-Left) layout support
- Custom Arabic fonts (ExpoArabic)
- Multi-language ready architecture

### 🎨 User Experience
- Modern and intuitive UI/UX
- Shimmer loading effects
- Smooth animations and transitions
- Image gallery viewer
- Share functionality
- Deep linking support
- Offline capability indicators

### 📞 Support & Information
- Contact us functionality
- About Aldaman Works
- Popular questions (FAQ)
- Terms and conditions
- Privacy policy
- Maintenance mode handling

### 🔒 Security & Performance
- Secure storage for sensitive data
- Encrypted API communication
- Crash reporting with Firebase Crashlytics
- Network error handling
- Image caching for performance
- App link protection

---

## 🧪 Testing

The project includes a comprehensive testing strategy to ensure code quality and reliability:

### Test Structure
- **Unit Tests**: Testing individual functions, use cases, and business logic
- **Widget Tests**: Testing UI components and user interactions
- **Integration Tests**: End-to-end testing of complete features
- **Repository Tests**: Testing data layer implementations
- **BLoC Tests**: Testing state management and business logic flows

### Running Tests

```bash
# Run all tests
flutter test

# Run tests with coverage
flutter test --coverage

# Run specific test file
flutter test test/widget_test.dart
```

### Test Coverage

The project aims for high test coverage across all layers:
- Domain layer: 90%+ coverage
- Data layer: 85%+ coverage  
- Presentation layer: 80%+ coverage

---

## 📁 Folder Structure

```
lib/
├── core/                          # Shared core functionality
│   ├── api/                       # API configuration and endpoints
│   ├── assets/                    # App constants and asset references
│   ├── controllers/               # Shared controllers
│   ├── database/                  # Local storage utilities
│   ├── enums/                     # Shared enumerations
│   ├── errors/                    # Error handling classes
│   ├── extensions/                # Dart extensions
│   ├── helpers/                   # Utility helper classes
│   ├── pages/                     # Shared pages
│   ├── routes/                    # App routing configuration
│   ├── service_locator/           # Dependency injection setup
│   ├── style/                     # App-wide styling
│   ├── themes/                    # Theme configuration
│   └── widgets/                   # Reusable widgets
│
├── features/                      # Feature modules
│   ├── Auth/                      # Authentication feature
│   │   ├── Data/
│   │   │   ├── DataSources/
│   │   │   ├── Models/
│   │   │   └── Repositories/
│   │   ├── Domain/
│   │   │   ├── Entities/
│   │   │   ├── Repositories/
│   │   │   └── UseCases/
│   │   └── Presentation/
│   │       ├── Controllers/
│   │       ├── Pages/
│   │       └── Widgets/
│   │
│   ├── booking/                   # Booking management
│   ├── cars/                      # Car rental & purchase
│   ├── home/                      # Home screen and browsing
│   ├── Notifications/             # Push notifications
│   ├── onboarding/                # Onboarding flow
│   ├── profile/                   # User profile
│   └── splash/                    # Splash screen
│
├── generated/                     # Auto-generated files
│   └── l10n/                      # Localization files
│
├── l10n/                          # Localization source files
│   └── *.arb                      # ARB files for translations
│
└── main.dart                      # App entry point

test/                              # Test files
assets/                            # Images, icons, fonts
android/                           # Android-specific files
ios/                               # iOS-specific files
web/                               # Web-specific files
```

---

## 🚀 How to Run the Project

### Prerequisites

- **Flutter SDK**: Version 3.6.1 or higher
- **Dart SDK**: Version 3.6.1 or higher
- **Android Studio** / **VS Code** with Flutter extensions
- **Xcode** (for iOS development, macOS only)
- **Firebase Account**: For push notifications and crash reporting

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd car_app
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Firebase Configuration**
   - Download `google-services.json` for Android and place it in `android/app/`
   - Download `GoogleService-Info.plist` for iOS and place it in `ios/Runner/`
   - Ensure Firebase projects are configured in Firebase Console

4. **Configure API Endpoints**
   - Update API base URLs in `lib/core/api/end_points.dart` if needed
   - Ensure backend services are accessible

5. **Generate Localization Files**
   ```bash
   flutter gen-l10n
   ```

6. **Run the app**
   ```bash
   # For Android
   flutter run

   # For iOS (macOS only)
   flutter run -d ios

   # For a specific device
   flutter devices
   flutter run -d [device-id]
   ```

### Build Instructions

#### Android APK
```bash
flutter build apk --release
```

#### Android App Bundle (for Play Store)
```bash
flutter build appbundle --release
```

#### iOS (requires macOS and Xcode)
```bash
flutter build ios --release
```

### Environment Setup

The app uses different API endpoints for different environments. Configure them in:
- `lib/core/api/end_points.dart`

### Key Configuration Files

- `pubspec.yaml` - Dependencies and assets
- `android/app/build.gradle` - Android build configuration
- `ios/Runner.xcodeproj` - iOS project configuration
- `firebase.json` - Firebase configuration
- `lib/firebase_options.dart` - Firebase initialization options

---

## 🔮 Future Improvements

### Planned Features
- [ ] **Payment Integration**: Direct in-app payment processing
- [ ] **Real-time Chat**: Customer support chat functionality
- [ ] **Video Tours**: 360° car view and video tours
- [ ] **Advanced Analytics**: User behavior tracking and analytics
- [ ] **Social Sharing**: Enhanced sharing with social media integration
- [ ] **Rating System**: User reviews and ratings for cars and services
- [ ] **Loyalty Program**: Rewards and loyalty points system
- [ ] **Multi-language**: Additional language support (English fully integrated)

### Technical Improvements
- [ ] **Performance Optimization**: Further code splitting and lazy loading
- [ ] **Caching Strategy**: Enhanced offline-first approach
- [ ] **CI/CD Pipeline**: Automated testing and deployment
- [ ] **Code Documentation**: Comprehensive API documentation
- [ ] **Error Tracking**: Enhanced error reporting and monitoring
- [ ] **Accessibility**: Improved accessibility features (a11y)
- [ ] **Dark Mode**: Theme switching support
- [ ] **Unit Test Coverage**: Increase test coverage to 90%+

### UX/UI Enhancements
- [ ] **Onboarding Improvements**: Interactive onboarding tutorial
- [ ] **Animation Polish**: Enhanced micro-interactions
- [ ] **Loading States**: More sophisticated loading indicators
- [ ] **Empty States**: Improved empty state designs

---

## 📸 Screenshots

<div align="center">

### Home Screen
<img src="screenshots/home.png" alt="Home Screen" width="250"/>

### Car Listing
<img src="screenshots/car_listing.png" alt="Car Listing" width="250"/>

### Car Details
<img src="screenshots/car_details.png" alt="Car Details" width="250"/>

### Booking Management
<img src="screenshots/bookings.png" alt="Bookings" width="250"/>

### Profile
<img src="screenshots/profile.png" alt="Profile" width="250"/>

</div>

> **Note**: Add actual screenshots to the `screenshots/` directory to display them here.

---

## 🔗 Social Links

<div align="center">

### Connect With Us

[![Website](https://img.shields.io/badge/Website-aldamanworks.com-blue)](https://aldamanworks.com)
[![Email](https://img.shields.io/badge/Email-Contact-orange)](mailto:info@aldamanworks.com)

### Development

**Company**: Aldaman Works  
**Country**: 🇸🇦 Saudi Arabia  
**Platform**: Mobile (iOS & Android)

---

### Contributors

We welcome contributions! Please feel free to submit a Pull Request.

---

<div align="center">

**Made with ❤️ in Saudi Arabia**

[⬆ Back to Top](#-aldaman-works---car-rental--purchase-app)

</div>
