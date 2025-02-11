# basic_url

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
# flutter_basic_url

`AndroidManifest.xml`
```xml
<queries>
        <!-- If your app checks for SMS support -->
        <intent>
            <action android:name="android.intent.action.VIEW" />
            <data android:scheme="sms" />
        </intent>
        <!-- If your app checks for call support -->
        <intent>
            <action android:name="android.intent.action.VIEW" />
            <data android:scheme="tel" />
        </intent>
        <!-- If your application checks for inAppBrowserView launch mode support -->
        <intent>
            <action android:name="android.support.customtabs.action.CustomTabsService" />
        </intent>
    </queries>
```


## 1
`pubspec.yaml`
```yaml
dependencies:
flutter:
sdk: flutter
url_launcher: ^6.0.20
```
`gradle-wrapper.properties`
```properties
distributionUrl=https\://services.gradle.org/distributions/gradle-8.10-all.zip
```

## 2
`debug`
```debug
What went wrong:
FAILURE: Build failed with an exception. * What went wrong: Execution failed for task ':url_launcher_android:compileDebugJavaWithJavac'. > Could not resolve all files for configuration ':url_launcher_android:androidJdkImage'. > Failed to transform core-for-system-modules.jar to match attributes {artifactType=_internal_android_jdk_image, org.gradle.libraryelements=jar, org.gradle.usage=java-runtime}. > Execution failed for JdkImageTransform: /Users/afrahman/Library/Android/sdk/platforms/android-34/core-for-system-modules.jar. > Error while executing process /Users/afrahman/Library/Java/JavaVirtualMachines/openjdk-23.0.2/Contents/Home/bin/jlink with arguments {--module-path /Users/afrahman/.gradle/caches/8.10/transforms/075e04261d13090900c86f63a6a0a19f-d606c5ae-af73-4fd8-b51e-f9330f4e5d74/transformed/output/temp/jmod --add-modules java.base --output /Users/afrahman/.gradle/caches/8.10/transforms/075e04261d13090900c86f63a6a0a19f-d606c5ae-af73-4fd8-b51e-f9330f4e5d74/transformed/output/jdkImage --disable-plugin system-modules}
``` 

solutoins:
`setting.gradle`
```gradle
plugins {
..
id "com.android.application" version "8.3.2" apply false
..
}
```


## References:
- https://www.cybrosys.com/blog/how-to-install-and-configure-flutter-url-launcher
- https://stackoverflow.com/questions/69619829/could-not-resolve-all-files-for-configuration-appandroidjdkimage
- https://www.youtube.com/watch?v=Wthmab2pI-o
