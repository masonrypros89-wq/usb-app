# USB Master - Offline Storage Utility

This project is a fully functional Android application source code designed to manage external USB storage devices entirely offline.

## Features
- **Fill Storage**: Fills the remaining space on the external device with random data to ensure no previous data is recoverable.
- **Wipe Storage**: Recursively deletes all files and directories on the device, including hidden content.
- **Format Utility**: Provides the choice to format the drive into **FAT32** or **exFAT**.
- **100% Offline**: Requires no internet permissions or connectivity.

## How to use with Android Studio
1. Unzip the `usb_master_project.zip` file.
2. Open **Android Studio**.
3. Select **"Open an Existing Project"**.
4. Navigate to the unzipped `usbmaster` folder and select it.
5. Wait for Gradle to sync.
6. Build and run the APK on your Android device.

## Important Note on Formatting
Due to Android's security model, third-party apps cannot perform low-level disk formatting (`mkfs`) directly. This app includes the logic to trigger the system's storage management interface to complete the format in the user's chosen filesystem (FAT32/exFAT).

## Permissions
The app requests `MANAGE_EXTERNAL_STORAGE` to ensure it can access all files, including hidden ones, for a complete wipe and fill operation.
