# android study link

https://kairo96.gitbooks.io/android/content/ch2.8.html

## creating a system overlay (always on top over all apps)
https://gist.github.com/bjoernQ/6975256

## transparent activity 
https://stackoverflow.com/questions/2176922/how-do-i-create-a-transparent-activity-on-android

~~~
Add the following style in your res/values/styles.xml file (if you don’t have one, create it.) Here’s a complete file:

<?xml version="1.0" encoding="utf-8"?>
<resources>
  <style name="Theme.Transparent" parent="android:Theme">
    <item name="android:windowIsTranslucent">true</item>
    <item name="android:windowBackground">@android:color/transparent</item>
    <item name="android:windowContentOverlay">@null</item>
    <item name="android:windowNoTitle">true</item>
    <item name="android:windowIsFloating">true</item>
    <item name="android:backgroundDimEnabled">false</item>
  </style>
</resources>
(The value @color/transparent is the color value #00000000 which I put in the res/values/color.xml file. You can also use @android:color/transparent in later Android versions.)

Then apply the style to your activity, for example:

<activity android:name=".SampleActivity" android:theme="@style/Theme.Transparent">
...
</activity>
~~~
