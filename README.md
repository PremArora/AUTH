# AuthApp - React Native Authentication

A modern React Native application demonstrating a complete authentication flow using React Context API, React Navigation, and AsyncStorage for state persistence.

## 🚀 Features

- **Authentication Flow**: Complete Signup, Login, and Logout functionality.
- **Global State Management**: Powered by React Context API (`AuthContext`) to manage user sessions across the app.
- **Persistent Sessions**: Uses `@react-native-async-storage/async-storage` to keep users logged in even after closing the app.
- **Dynamic Navigation**: Conditional routing using `@react-navigation/native-stack` (Auth Stack vs. Protected Home Stack).
- **Form Validation**: robust client-side validation for email formats, password lengths, and required fields.
- **Modern UI/UX**: Clean, responsive layout with loading states and password visibility toggles (👁️).

## 🛠️ Tech Stack

- **Framework**: React Native (0.81.1)
- **State**: React Context API
- **Navigation**: React Navigation 7
- **Storage**: AsyncStorage 1.24.0
- **Language**: TypeScript

## 🏗️ Getting Started

### 1. Install Dependencies
```sh
yarn install
```

### 2. Android Setup (Important)
Due to a known dependency resolution issue in newer AsyncStorage versions, this project uses version `1.24.0`. Ensure `mavenCentral()` is included in your `android/build.gradle`:

```gradle
allprojects {
    repositories {
        google()
        mavenCentral()
    }
}
```

### 3. Run the App
```sh
# Start Metro Bundler
yarn start

# Run on Android
yarn android

# Run on iOS
cd ios && pod install && cd ..
yarn ios
```

## 📁 Project Structure

- `src/context/AuthContext.tsx`: Core authentication logic and storage persistence.
- `src/navigation/AppNavigator.tsx`: Main navigation tree and protected route logic.
- `src/screens/`:
  - `LoginScreen.tsx`: Modern login form with validation.
  - `SignupScreen.tsx`: User registration form.
  - `HomeScreen.tsx`: Protected dashboard showing user profile info.
