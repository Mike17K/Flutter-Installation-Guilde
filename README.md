# Run Flutter Setup Steps

# Install Java JDK

Install Java JDK from [here](https://www.oracle.com/java/technologies/downloads/) or [Download](https://download.oracle.com/java/20/latest/jdk-20_windows-x64_bin.exe).

installed in location by default C:\Program Files\Java\jdk-20
create a JAVA_HOME enviroment variable and set it to "C:\Program Files\Java\jdk-20"

# Install Android Studio

- From the android studio [download page](http://android.cn-mirrors.com/sdk/index.html#win-bundle) download the windows file or [download it here](https://dl.google.com/dl/android/studio/install/1.0.1/android-studio-bundle-135.1641136.exe).

follow the installation process

if this doesn't operate try [here](https://developer.android.com/studio)

# Install Dart SDK

To run a Flutter app, you need to have the Dart SDK installed on your system. Flutter is a framework that uses the Dart programming language, and the Dart SDK provides the necessary tools to compile, run, and debug Dart code.

- install it from the official [website](https://dart.dev/get-dart) or run as admin

```
choco install dart-sdk
```

# Install Flutter SDK

Go to official [website](https://docs.flutter.dev/get-started/install/windows) and follow the instructions or do the steps bellow

1. [download](https://storage.googleapis.com/flutter_infra_release/releases/stable/windows/flutter_windows_3.7.12-stable.zip) the zip SDK 3.7.12
2. Extract the zip file in the desired location, suggest **C:\src**.
3. Add Flutter path (**C:\src\flutter\bin**) in the User PATH environment variables, to do it write in the windows search "μεταβλητές συστήματος" -> "μεταβλητές περιβάλλοντος" -> "μεταβλητές χρήστη" -> "path" -> "δημιουργία" -> paste **C:\src\flutter\bin** -> "ok" -> "ok" -> "ok".
4. Test if it works, run in cmd

```
$ where flutter dart
```

the output should be

```
C:\src\flutter\bin\flutter
C:\src\flutter\bin\flutter.bat
C:\src\flutter\bin\dart
C:\src\flutter\bin\dart.bat
C:\tools\dart-sdk\bin\dart.exe
```

execute

```
$ flutter pub get
```

5. Test for errors with

```
$ flutter doctor
```

# Run Emulator Android studio

Tools -> Device Manager
create a device, and run it from the "Play" button (green triangle).

This may take some time, especially the first time you start the emulator or if you are using a slow computer.

# Run Flutter

Create project, and run it select target device and run (f5) from main.dart

# Troubleshooting

### Flutter doctor error - Android sdkmanager tool not found. Windows

The key is to install Android SDK Command-line Tools, steps being:

1. Open Android Studio
2. Tools -> SDK Manager -> Android SDK -> SDK Tools -> check "Android SDK Build-Tools 34-rc3" -> Apply -> ok

![SDK Manager installations Page](https://i.stack.imgur.com/nHCyV.jpg)
