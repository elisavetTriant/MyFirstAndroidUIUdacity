# Basic Android Development, My first simple UI

This is a small Android Studio 3 project that outputs a greeting card. This was made for the  Google Developer Challenge 2017-2018 as an assignment to practice with Layouts, TextViews and ImageViews.

This is how the Card looks like on Android Studio 3:

![Greeting Card](https://github.com/elisavetTriant/MyFirstAndroidUIUdacity/blob/master/screenshots/androidstudio_myfirstUIUdacity.png "Greeting Card")

And here is what the layout xml code looks like (file app->src->main->res->layout->activity_main.xml):
```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="@color/colorPrimaryDark"
    tools:context="co.elisavet.udacitymyfirstui.MainActivity">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/wish"
        android:padding="16dp"
        style="@style/messagesTextStyle" />


    <ImageView
        android:id="@+id/photo_image_view"
        android:layout_width="match_parent"
        android:layout_height="0dp"
        android:scaleType="centerCrop"
        android:layout_weight="1"
        android:src="@drawable/sunrise" />

    <TextView
        android:layout_width = "match_parent"
        android:layout_height = "wrap_content"
        android:text="@string/message"
        android:padding="16dp"
        style="@style/messagesTextStyle" />


    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="@string/credits"
        android:padding="10dp"
        android:background="@color/creditsbackgroundColor"
        style="@style/creditsTextStyle" />

</LinearLayout>
```
Don't forget to take a look at the resources folder (app->res->values) and take a look at the code there also. 
For instance the strings.xml resource looks like this:
```xml
<resources>
    <string name="app_name">UdacityMyFirstUI</string>
    <string name="credits">Made with love by @EliTriant</string>
    <string name="wish">Rise and shine! It\'s time for yoga!</string>
    <string name="message">To all my yoga friends!</string>
</resources>
```
The colors.xml resource looks like this:
```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="colorPrimary">#3F51B5</color>
    <color name="colorPrimaryDark">#303F9F</color>
    <color name="colorAccent">#FF4081</color>
    <color name="creditsbackgroundColor">#999999</color>
</resources>
```

The styles.xml resource looks like this:
```xml
<resources>
    <!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light.DarkActionBar">
        <!-- Customize your theme here. -->
        <item name="colorPrimary">@color/colorPrimary</item>
        <item name="colorPrimaryDark">@color/colorPrimaryDark</item>
        <item name="colorAccent">@color/colorAccent</item>
    </style>

    <style name="messagesTextStyle">
        <item name="android:textColor">@android:color/white</item>
        <item name="android:textAlignment">center</item>
        <item name="android:textSize">24sp</item>
    </style>

    <style name="creditsTextStyle">
        <item name="android:textColor">@android:color/black</item>
        <item name="android:textAlignment">center</item>
        <item name="android:textSize">12sp</item>
    </style>
</resources>
```
More on Resources on [https://developer.android.com/guide/topics/resources](https://developer.android.com/guide/topics/resources)