## Sakeshioyaki
fix permission to record in android 13 &&  width, height of device

# ED Flutter Screen Recorder

Screen recorder plugin for Flutter. Supports IOS and Android devices.It does not work on the IOS emulator!!!!

Fork from : 
[![pubdev](https://img.shields.io/badge/pub-de__screen__recorder-blue)](https://pub.dev/packages/ed_screen_recorder)

## Using

pubspec.yaml
```yaml
ed_screen_recorder:
git : "https://github.com/Sakeshioyaki/ed_screen_recorder"
```

android/app/src/main/AndroidManifest.xml
```xml
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" android:maxSdkVersion="32" tools:ignore="ScopedStorage" /> 
    <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" android:maxSdkVersion="32" />
<!--    <uses-permission android:name="android.permission.MANAGE_EXTERNAL_STORAGE" android:maxSdkVersion="32" tools:ignore="ScopedStorage" /> -->
    <uses-permission android:name="android.permission.RECORD_AUDIO" /> 
    <uses-permission android:name="android.permission.FOREGROUND_SERVICE" />
```

You only need add the permission message on the Info.plist

```
  <key>NSPhotoLibraryUsageDescription</key>
	<string>Save video in gallery</string>
	<key>NSMicrophoneUsageDescription</key>
	<string>Save audio in video</string>

```
  
## Feedback

If you have any feedback, please contact us at ringo150299@gmail.com

