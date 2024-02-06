This app is companion of [NPS app](https://github.com/yurpetr/nps)  for Android tablets (checked on Samsung Galaxy Tab 3 with Android 7.1)
App working in Kiosk Mode. Disable screen lock on system settings

Change URL in MainActivity.java into your own NPS app
```
webView.loadUrl("http://nps.yourdomain.com/");
```

Make app "Device Admin" in system settings
OR
```
adb shell dpm set-active-admin com.yurpetr.npsapp/com.yurpetr.npsapp.AdminReceiver
```

Make app "Device owner" via ADB
```
adb shell dpm set-device-owner com.yurpetr.npsapp/com.yurpetr.npsapp.AdminReceiver
```
Remove via 
```
adb shell dpm remove-active-admin com.yurpetr.npsapp/com.yurpetr.npsapp.AdminReceiver
```
