# How to reproduce

First, install dependencies

```bash
npm install
```

## With Development Build

```bash
npx expo run:android
```

On the home screen, click the "ENABLE BACKGROUND LOCATION" button, and the following output should appear in the console:

```
LOG  Foreground permission granted
LOG  Background permission granted
LOG  Background service started
```

And the background location service is successfully registered, which can be verified by clicking the "CHECK REGISTERED TASKS" button:

```
LOG  Registered tasks:
LOG  [{"options": {"accuracy": 3, "foregroundService": [Object], "mayShowUserSettingsDialog": true}, "taskName": "background-location-task", "taskType": "location"}]
```

However, the requested location data are never obtained.


## With Expo Go

Start the app

```bash
npx expo start
```

Open in Expo Go in Android, click the "ENABLE BACKGROUND LOCATION" button in the home page, and the warning should appear:

```
Error: Call to function 'ExpoLocation.startLocationUpdatesAsync' has been rejected.
→ Caused by: Couldn't start the foreground service. Foreground service permissions were not found in the manifest
```

Tested with an Android emulator of the Pixel_3a_API_34_extension_level_7_x86_64 model
