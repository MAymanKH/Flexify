<div align = "center">
<img src = "https://i.imgur.com/zUDmmyy.png" width = 200>

# **Flexify - Wallpapers & Widgets**

[![GitHub stars](https://img.shields.io/github/stars/mayman007/flexify?style=social)](https://github.com/mayman007/flexify/stargazers)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Flutter](https://img.shields.io/badge/Flutter-%2302569B.svg?style=flat&logo=Flutter&logoColor=white)](https://flutter.dev/)

<a href='https://play.google.com/store/apps/details?id=com.maymanxineffable.flexify'><img alt='Get it on Google Play' src='https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png' height="80"/></a>

</div>

## Table of Contents

- [Why Flexify?](#why-flexify)
- [Features](#features)
- [Getting Started](#getting-started)
- [Community](#community)
- [Screenshots](#screenshots)
- [Running from Source Code](#running-from-source-code)
- [Built With](#built-with)
- [Contributing](#contributing)
- [Support](#support)
- [License](#license)

## Why Flexify?

Flexify is more than just a personalization app; it’s your gateway to making your phone reflect *you*. Whether you prefer minimalism, vibrant colors, or intricate designs, Flexify has you covered.

## Features

| Content & Aesthetics | User Experience |
|:--- |:--- |
| 🖼️ **600+ 4K Wallpapers** <br> A massive collection for every taste. | 💾 **High Quality Downloads** <br> Save your favorites in full resolution. |
| 📱 **Widgets & Live Walls** <br> 100+ KWGT widgets & KLWP wallpapers. | 💙 **Favorites System** <br> Keep track of wallpapers or widgets you love. |
| 🎨 **Dynamic Theming** <br> Material You support with 10+ color schemes. | 📋 **Smart Categorization** <br> Easy navigation through organized content. |
| 🎭 **Material Design 3** <br> Fluid animations and beautiful UI. | 🌍 **Multi-language** <br> Supports English, Arabic, and Hindi. |

## Getting Started

### Download the App

Download Flexify directly from [Google Play Store](https://play.google.com/store/apps/details?id=com.maymanxineffable.flexify).

### Requirements

- Android 5.0 or later.
- KWGT and KLWP apps installed (for widgets and depth wallpapers).

## Community

Join our growing community on Telegram to share your setups, get inspiration, and stay updated with the latest releases:  
[Flexify Telegram Channel](https://t.me/Flexify_updates)  

# Screenshots

| ![Image 1](https://i.imgur.com/BoaWX10.jpeg) | ![Image 2](https://i.imgur.com/0DSRMiB.jpeg) | ![Image 3](https://i.imgur.com/A5PTTOe.jpeg) |
|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| ![Image 4](https://i.imgur.com/qvc0og8.jpeg) | ![Image 5](https://i.imgur.com/7K5Ok3U.jpeg) | ![Image 6](https://i.imgur.com/tdXNoad.jpeg) |

## Running from Source Code

### Prerequisites

- [Flutter](https://docs.flutter.dev/get-started/install) SDK (3.32 recommended)
- [Android Studio](https://developer.android.com/codelabs/basic-android-kotlin-compose-install-android-studio#2) or [VS Code](https://code.visualstudio.com/download) with Flutter extensions
- [Firebase](https://firebase.google.com/) account
- [Git](https://git-scm.com/downloads)

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/mayman007/flexify.git
   cd flexify
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Firebase Setup**
   - Create a new Firebase project at [Firebase Console](https://console.firebase.google.com/)
   - Enable Firebase Analytics and Crashlytics
   - Download `google-services.json` and place it in `android/app/`
   - Add your app's package name: `com.maymanxineffable.flexify`

4. **API Configuration**
   - Setup [Flexify API](https://github.com/mayman007/flexify-api) to fetch content as shown in [its instructions](https://github.com/mayman007/flexify-api?tab=readme-ov-file#installation)
   - Add the following API endpoints to [Firebase remote configs](https://firebase.google.com/docs/remote-config/get-started?platform=flutter#set-parameter)
      - hq wallpapers endpoint as `walls_hq`
      - mid wallpapers endpoint as `walls_mid`
      - low wallpapers endpoint as `walls_low`
      - depth walls endpoint as `depth_walls`
      - widgets endpoint as `widgets`
      - `{"X-Custom-Header": ""}` as `api_headers` (currently empty header)
   - The API provides wallpapers, widgets, and depth wallpapers data

5. **Build and Run**
   ```bash
   # For debug build
   flutter run
   
   # For release build
   flutter build apk --release
   ```

### Project Structure

- `lib/src/provider/` - API integration and data providers
- `lib/src/views/` - App screens and UI
- `lib/src/widgets/` - Custom widgets and components
- `assets/translations/` - Localization files
- `android/` - Android-specific configuration

## Built With

- [Flutter](https://flutter.dev/) - UI Toolkit
- [Flexify API](https://github.com/mayman007/flexify-api) - Backend content server
- [Firebase](https://firebase.google.com/) - Remote config & Analytics
- [Provider](https://pub.dev/packages/provider) - State Management
- [Dio](https://pub.dev/packages/dio) - Networking
- [SQFlite](https://pub.dev/packages/sqflite) - Local Database
- [Dynamic Color](https://pub.dev/packages/dynamic_color) - Material You Theming

## Contributing

We welcome contributions to make Flexify even better! Here are the ways you can help:

### 🌍 Translation Contributions

Help us make Flexify accessible to more people by adding your language or improving existing translations.

#### Adding a New Language

1. **Fork the repository** and clone it to your local machine
2. **Navigate to the translations folder**: `assets/translations/`
3. **Create a new JSON file** for your language using the ISO 639-1 language code (e.g., `fr.json` for French, `es.json` for Spanish)
4. **Copy the structure** from `en.json` and translate all the values to your language
5. **Test your translation** by [setting up](https://github.com/mayman007/Flexify?tab=readme-ov-file#setup-nstructions) and running the app, then switching to your language (optional)
6. **Submit a pull request** with your translation

#### Translation Guidelines

- Keep translations **concise and natural** in your language
- Maintain the **same tone** as the English version (friendly and professional)
- Test translations in the app to ensure they **fit the UI properly** (optional, but recommended)
- For technical terms (like "KWGT", "KLWP"), keep them as-is unless there's a widely accepted translation
- Use **gender-neutral language** where possible
- Follow your language's **capitalization conventions**

## Support

Have questions, feedback, or issues? We’d love to hear from you! Contact us at:

- **Open an [Issue](https://github.com/mayman007/Flexify/issues)**
- **Join [Telegram Discussion Group](https://t.me/Flexify_discussion)**

## License

This project is licensed under the **GNU Affero General Public License v3.0** - see the [LICENSE](LICENSE) file for details.
