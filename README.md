# Sample code

## I. Add dependency library

Don't change library version

```groovy
    // GOOGLE ADMOB
    implementation 'com.google.android.gms:play-services-ads:24.7.0'
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
        <meta-data
            android:name="com.google.android.gms.ads.APPLICATION_ID"
            android:value="ca-app-pub-3940256099942544~3347511713" /> <!-- Change to real ADMOB APPID -->
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