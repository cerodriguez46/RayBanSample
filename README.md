# SynthHumLab Ray-Ban Tracker 👓

[![Project Code Linting](https://github.com/cerodriguez46)](https://github.com/cerodriguez46/RayBanSample)

An advanced iOS application built using SwiftUI that interfaces securely with **Ray-Ban Meta Smart Glasses** utilizing the official Meta Wearables Device Access Toolkit (DAT).

---

## 🚀 Features
* **Secure Architecture:** Decoupled local credential configurations using `.xcconfig` templates to keep developer tokens off public repositories.
* **Automated Linting:** Lightweight GitHub Actions pipeline to validate code workspace integrity on every push.
* **App Store Ready:** Pre-built `docs/` architecture linked directly to a public GitHub Pages deployment for required Privacy Policies and Terms of Service.

---

## 🛠️ Local Prerequisites
To download, compile, and run this project with physical smart glasses, you must have:
* **Mac Hardware:** Running macOS Sonoma (or newer) with Xcode 15.4+ installed.
* **Apple Developer Account:** Required for native background Bluetooth & external accessory code signing.
* **Meta Wearables Developer Profile:** Registered via the [Meta Wearables Developer Center](https://meta.com).
* **Developer Mode Enabled:** Open the **Meta AI** companion app on your phone, navigate to your device settings, and tap the application version string 5 to 7 times until the Developer Options menu unlocks.

---

## 📦 Getting Started & Installation

### 1. Clone the Repository
```bash
git clone https://github.com
cd YOUR_REPOSITORY_NAME
```

### 2. Configure Your Secret Developer Tokens
Because this repository is public, your specific Meta credentials are blocked via the `.gitignore` rules. You **must** create your own local configuration card before hitting compile:

1. Open the project workspace in Xcode.
2. In the root directory, create a new configuration file named exactly: `DeveloperKeys.xcconfig`
3. Paste your custom sandbox tokens from your Meta Wearables dashboard into it:
   ```text
   META_APP_ID = YOUR_META_APP_ID_HERE
   META_CLIENT_TOKEN = YOUR_META_CLIENT_TOKEN_HERE
   ```

### 3. Open and Build the App
1. Connect your **physical iOS device** via a USB cable (The iOS Simulator does not support the low-level Bluetooth accessory pipeline required by the glasses).
2. Ensure **Developer Mode** is turned on under *Settings > Privacy & Security* on your iPhone.
3. Select your physical device target in the top toolbar of Xcode.
4. Press `⌘ + R` to compile, resolve Swift Package dependencies, and deploy live!

---

## 🔒 Data & Privacy Policy
This application processes all camera, microphone, and sensor telemetry data stream assets **locally and in real-time** on the host iOS device. No hardware telemetry or media streams are stored, shared, or transmitted to external third-party cloud architectures. 

For full legal terms, view our public live tracking configurations:
* [Live Privacy Policy](https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/privacy)
* [Live Terms of Use](https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/terms)

## 📄 License
This repository is licensed under the terms of the [MIT License](LICENSE).

