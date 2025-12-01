# 🚗 Aldaman Works - Car Rental & Purchase App

<div align="center">

**A comprehensive Saudi Arabian mobile application for car rental and purchase services**

[![Flutter](https://img.shields.io/badge/Flutter-3.6.1-blue.svg)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-3.6.1-blue.svg)](https://dart.dev/)
[![License](https://img.shields.io/badge/License-Private-red.svg)]()
[![Google Play](https://img.shields.io/badge/Google_Play-Download-blue.svg)](https://play.google.com/store/apps/details?id=com.aldaman_works.aldaman_works)
[![App Store](https://img.shields.io/badge/App_Store-Download-black.svg)]([https://apps.apple.com/app/aldaman-works/id[APP_ID]](https://apps.apple.com/sa/app/%D8%A3%D8%B9%D9%85%D8%A7%D9%84-%D8%A7%D9%84%D8%AF%D9%85%D8%B9%D8%A7%D9%86-%D9%84%D9%84%D8%B3%D9%8A%D8%A7%D8%B1%D8%A7%D8%AA/id6749268138))
[![Saudi Arabia](https://img.shields.io/badge/Country-🇸🇦_Saudi_Arabia-green.svg)]()
[![Version](https://img.shields.io/badge/Version-1.0.10-orange.svg)]()

[Features](#-features) • [Architecture](#-architecture) • [Download](#-download--installation) • [Structure](#-folder-structure) 

</div>

---

## 📱 Project Overview

**Aldaman Works** is a full-featured mobile application developed for the Saudi Arabian market, providing seamless car rental and purchase services. The app enables users to browse available vehicles, make reservations, purchase cars with flexible payment options (cash or financing), manage bookings, and interact with multiple branches across the Saudi Arabian.

### Key Highlights
- 🇸🇦 **Saudi-focused**: Built specifically for the Saudi Arabian market with Arabic language support
- 🚀 **Production-ready**: Version 1.0.10+35 deployed and actively maintained
- 🏗️ **Scalable Architecture**: Clean Architecture with feature-based modular design
- 🔒 **Secure**: Secure storage, token-based authentication, and encrypted communication
- 📱 **Cross-platform**: Supports both iOS and Android platforms

---

## 📥 Download & Installation

Get Aldaman Works on your mobile device:

<div align="center">

### 📱 Available on

[![Google Play Store](https://img.shields.io/badge/Download_on_Google_Play-3DDC84?style=for-the-badge&logo=google-play&logoColor=white)](https://play.google.com/store/apps/details?id=com.aldaman_works.aldaman_works)
[![App Store](https://img.shields.io/badge/Download_on_App_Store-0D96F6?style=for-the-badge&logo=app-store&logoColor=white)](https://apps.apple.com/sa/app/%D8%A3%D8%B9%D9%85%D8%A7%D9%84-%D8%A7%D9%84%D8%AF%D9%85%D8%B9%D8%A7%D9%86-%D9%84%D9%84%D8%B3%D9%8A%D8%A7%D8%B1%D8%A7%D8%AA/id6749268138)


### 📊 App Information

| Detail | Android | iOS |
|--------|---------|-----|
| **Version** | 1.0.10 | 1.0.10 |
| **Size** | ~11 MB | ~37 MB |
| **Language** | Arabic | English |

</div>

---

## 🛠️ Tech Stack

### Core Framework
- **Flutter** `3.38.3` - Cross-platform UI framework

### State Management
- **flutter_bloc** `^9.1.0` - BLoC pattern implementation

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
- **firebase_analytics** `^11.0.0` - App analytics and user behavior tracking
- **firebase_remote_config** `^5.0.0` - Remote configuration management

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

### 📊 Analytics & Remote Configuration
- **Firebase Analytics**: Comprehensive user behavior tracking
- **Remote Config**: Dynamic feature flags and app configuration
- Real-time analytics for car views, searches, bookings, and user engagement
- A/B testing capabilities through remote configuration
- Dynamic feature toggles without app updates

---

## 🧪 Testing

The project includes a comprehensive testing strategy to ensure code quality and reliability:

### Test Structure
- **Unit Tests**: Testing individual functions, use cases, and business logic
- **Widget Tests**: Testing UI components and user interactions
- **Integration Tests**: End-to-end testing of complete features
- **Repository Tests**: Testing data layer implementations
- **BLoC Tests**: Testing state management and business logic flows


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


## 📊 Firebase Analytics & Remote Config

### Analytics Implementation

The app includes comprehensive analytics tracking using Firebase Analytics to monitor user behavior and app performance:

#### Tracked Events
- **App Events**: App opens, screen views, user engagement
- **User Events**: Login, signup, profile updates
- **Car Events**: Car views, searches, filters, favorites
- **Booking Events**: Checkout starts, purchases, cancellations
- **Navigation Events**: Screen transitions and user flow
- **Error Events**: App errors and crashes
- **Feature Usage**: Custom feature interactions

### Best Practices

#### Analytics
- Track meaningful user actions, not every button tap
- Use consistent naming conventions for events and parameters
- Set user properties for better segmentation
- Monitor analytics data regularly to improve user experience

#### Remote Config
- Always provide sensible default values
- Use feature flags for gradual rollouts
- Test configuration changes in development first
- Monitor impact of configuration changes on user behavior

---

## 📸 Screenshots

<div align="center">

### Home Screen
<img src="https://github.com/user-attachments/assets/429766e0-dac6-4412-b49f-b62f35173dd8" alt="Home Screen" width="250"/>

### Car Listing
<img src="https://github.com/user-attachments/assets/c16e571f-b107-4088-8f6e-c8f2e01c59a5" alt="Car Listing" width="250"/>

### Car Details
<img src="https://github.com/user-attachments/assets/4b206de4-2e46-458b-9485-2deb0767f1a8" alt="Car Details" width="250"/>

### Booking Management
<img src="https://github.com/user-attachments/assets/20d7f77c-4309-4d7c-8705-d9a0c973aaea" alt="Bookings" width="250"/>

### Profile
<img src="https://github.com/user-attachments/assets/82f0b1db-ce97-4e61-b99c-39d5d59e9e24" alt="Profile" width="250"/>

</div>


---

## 👨‍💻 Developer & Contact

<div align="center">

### **Ahmed Nasr**
**Flutter Developer & Mobile App Specialist**

📧 **Email**: ahmed.nasr.fahmey@gmail.com  
🌐 **LinkedIn**: https://www.linkedin.com/in/ahmed-nasr-fahmey/


---

</div>

[⬆ Back to Top](#-aldaman-works---car-rental--purchase-app)

</div>
