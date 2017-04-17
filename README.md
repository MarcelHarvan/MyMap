# MyMap [![MyWeb](http://marcelharvan.com/images/glyphicons-341-globe.png)](http://marcelharvan.com)
A simple Android app showing your current position.

## Requirements
- Android Studio 2.3.1 or grater
- [Google Maps API](https://developers.google.com/maps/documentation/javascript/get-api-key)

## Steps 
- Create a new Android Studio project
- Select Google Maps Activity
- AndroindManifest.xml add: 
 
```xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```
 - add your API to google_maps_api.xml
 ```xml
 <string name="google_maps_key" templateMergeStrategy="preserve" translatable="false">Your API!!</string>
 ```
 
 - create a GPSTracker class extends Service implements LocationListener.
 Neccesary aditional Override methods: 
 
  ```java
  @Override
    public void onStatusChanged(String s, int i, Bundle bundle) { }

    @Override
    public void onProviderEnabled(String s) { }

    @Override
    public void onProviderDisabled(String s) {}

    @Nullable
    @Override
    public IBinder onBind(Intent intent) {return null;}

    @Override
    public void onLocationChanged(Location location) {}
    
    // all the code is in GPSTracker.java
 ```
- do some changes in MapsActivity.java
- run app



