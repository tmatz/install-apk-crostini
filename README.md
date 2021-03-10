# Install APK for Chromebook(arm64)

## How to develop android application on chromebook(arm64)

1. Enable `ADB Debug` on Linux.

2. Use AIDE (android app) for develop android application.

- Do install app. It will fail, but it's OK.

3. Launch `Install APK` app (it's in Linux folder on desktop), and press Install button.

## What does Install APK do

First, the program pulls .apk from android, then place it in /tmp directory inside Linux(crostini).

```
$ adb pull /mnt/sdcard/Android/data/com.aide.ui/cache/apk/app.apk /tmp/app.apk
```

Then install it.

```
$ adb install /tmp/app.apk
```
