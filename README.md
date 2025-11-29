# first-watch-face

On the watch:
 - Enable Developer options.
 - Turn on ADB debugging and Wireless debugging.

```sh
adb pair <WATCH_IP>:<PAIRING_PORT>
adb connect <WATCH_IP>:<ADB_PORT>
gradlew.bat installDebug
adb shell am broadcast -a com.google.android.wearable.app.DEBUG_SURFACE --es operation set-watchface --es watchFaceId com.example.codelab
```

I should change com.example.codelab to my app ID

From WFS to WFF to watch:
✅ WFS → Publish → get .aab (or Run on Watch)
✅ Unzip .aab → base/res/raw/watchface.xml.
✅ Copy to this project
✅ Replace its res/raw/watchface.xml + drawables with WFS equivalent
✅ gradlew.bat installDebug
✅ Optionally adb shell am broadcast ... 