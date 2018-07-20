# OpenCV-With-Android

![opencv](https://github.com/tlhcelik/OpenCV-with-Android/blob/master/opencv-android.png)

OpenCV download [Link](https://sourceforge.net/projects/opencvlibrary/files/opencv-android/3.4.0/opencv-3.4.0-android-sdk.zip/download) version is 3.4.0

**Importing OpenCV SDK**
1) Extract opencv_xxx_sdk.zip
2) Android Studio -> File -> import module -> select contain file in __java__ folder
3) Android Studio -> File -> Project Structure -> app -> click + button -> select opencv-xxx-sdk

**Build Gradle Settings for OpenCV :**
```java
apply plugin: 'com.android.library'

android {
    compileSdkVersion 23 // SDK version must be 23
    buildToolsVersion "27.0.3" // build version 

    defaultConfig {
        minSdkVersion 8 
        targetSdkVersion 23 // target version 23 or 24, 25 ,26 ,...
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.txt'
        }
    }
}
```
**Get Camera Permissions On AndroidManifest.xml**
```xml
  <uses-permission android:name="android.permission.CAMERA"/>
```

**activity_main.xml design**
  ```xml
  <org.opencv.android.JavaCameraView
  android:layout_width="match_parent"
  android:layout_height="match_parent"
  android:visibility="gone"
  android:id="@+id/tutorial1_activity_java_surface_view"/>
```
