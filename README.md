# Sample code

## I. Add dependency library

Don't change library version

```groovy
    // APPLOVIN
    implementation 'com.adjust.sdk:adjust-android:4.28.7'
    implementation("com.applovin:applovin-sdk:12.1.0@aar")

    //FACEBOOK
    implementation 'androidx.annotation:annotation:1.7.0'
    implementation 'com.facebook.android:audience-network-sdk:6.16.0'

    // GOOGLE ADMOB
    implementation 'com.google.android.gms:play-services-ads:22.5.0'

    // UNITY
    implementation 'com.unity3d.ads:unity-ads:4.9.2'
```

## II. Add permission

add to `AndroidManifest.xml`

```xml
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="com.google.android.gms.permission.AD_ID" />
    <uses-permission android:name="com.google.android.finsky.permission.BIND_GET_INSTALL_REFERRER_SERVICE" />
    <queries>
        <package android:name="com.android.vending" />
        <package android:name="com.facebook.katana" />
    </queries>
```

## III. Add Meta Data

```xml
    <Application ...>
        <!-- Replace your admob APPLICATION_ID here -->
        <meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-3940256099942544~3347511713" />

        <meta-data
            android:name="com.google.android.gms.ads.DELAY_APP_MEASUREMENT_INIT"
            android:value="true" />
    
    </Application>        
```


## IV. Keep classes

add to `proguard-rules.pro`

```text

-keep class com.google.** { *; }
-keep class com.unity3d.** { *; }
-keep class com.applovin.** { *; }
-keep class com.adjust.** { *; }
-keep class com.appsflyer.** { *; }
-keep class com.facebook.** { *; }
```
