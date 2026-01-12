# AR Assistant

A modern **AI-powered chat assistant** built with Flutter, featuring real-time voice-to-text input, quick report generation, beautiful UI with dark/light mode, and robust error handling with retry functionality.

Perfect for AR (Augmented Reality) related queries, report generation, and interactive conversations.

## ✨ Features

- **Real-time Chat Interface** using `flutter_chat_ui` + `flutter_chat_core`
- **Voice-to-Text Input** (tap-to-speak / auto-stop on silence)
- **Quick Reports** chips (Client-wise, Bucket-wise, Age-wise, Collection Projection)
- **Smart Text Correction** (e.g., "afta" → "AFDA", "list all the" → special commands)
- **API Integration** with Dio + Pretty Logger
- **Retry Mechanism** for failed messages
- **Dark / Light Mode** with smooth theme switching
- **Image Message Support** (camera + gallery)
- **Custom Drawer** with theme toggle
- **Dynamic API Timeout** configuration
- **Beautiful UI** with animations, shimmer loading, and modern design

## 🚀 Tech Stack

- **Framework**: Flutter (Dart)
- **Chat UI**: flutter_chat_ui, flutter_chat_core
- **Voice Recognition**: speech_to_text
- **HTTP Client**: Dio + pretty_dio_logger
- **Permissions**: permission_handler
- **Image Picker**: image_picker + insta_image_viewer
- **State Management**: Provider (for theme), setState for local UI
- **Storage**: shared_preferences (for timeout settings)
- **Other**: uuid, shimmer, flutter_keyboard_visibility, flutter_speed_dial

## 📦 Installation

```bash
# Clone the repo
git clone https://github.com/yourusername/ar-assistant.git

# Go to project directory
cd ar-assistant

# Install dependencies
flutter pub get

# Run on device/emulator
flutter run
```

# Android Setup (Important!)

Add to android/app/src/main/AndroidManifest.xml:

```xml
<uses-permission android:name="android.permission.RECORD_AUDIO" />
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

# Configuration

1. API Endpoint
   Update ApiConfig.BASE_URL in lib/api/api_config.dart

2. Change API Timeout
   Drawer → "Set Timeout Limit" → select 30s / 60s / 120s / etc.

3. Voice Language
   Currently set to en_IN (Indian English) — change in VoiceToTextModal

# Development Commands

```bash
# Run in debug mode
flutter run

# Build APK (release)
flutter build apk --release

# Clean project
flutter clean && flutter pub get

# Generate launcher icons (if needed)
flutter pub run flutter_launcher_icons
```
