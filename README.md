# How to reproduce

1. Install dependencies

   ```bash
   npm install
   ```

2. Start the app

   ```bash
   npx expo start
   ```

3. Open in Expo Go in Android, click the "ENABLE BACKGROUND LOCATION" button in the home page, and the warning should appear:

```
Error: Call to function 'ExpoLocation.startLocationUpdatesAsync' has been rejected.
-> Caused by: Couldn't start the foreground service. Foreground service permissions were not found in the manifest
```

Tested with an Android emulator of the Pixel_3a_API_34_extension_level_7_x86_64 model
