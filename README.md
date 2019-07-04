# RNChatkitDemo
A simple chat app built with React Native and Chatkit which has the following features:

-  Public and private chat rooms
-  Roles and permissions
-  Typing indicators
-  Read receipt
-  File uploads
-  Show online and offline users

## Installation

1.  Clone the repo:

```
git clone https://github.com/dpericic/Chat-Application-using-Chatkit.git
```

2.  Install the app dependencies:

```
npm install
```

3.  Link the packages:

```
react-native link react-native-gesture-handler
react-native link react-native-permissions
react-native link react-native-document-picker
react-native link react-native-fs
react-native link react-native-config
react-native link react-native-vector-icons
react-native link rn-fetch-blob
```

('react-native-audio-toolkit' will require manual linking)

4.  Update `android/app/build.gradle` file:

```
apply from: "../../node_modules/react-native/react.gradle"

// add these:
apply from: "../../node_modules/react-native-vector-icons/fonts.gradle"
apply from: project(':react-native-config').projectDir.getPath() + "/dotenv.gradle"
```

5. Update `android/app/src/main/AndroidManifest.xml` to add permission to read from external storage:

```
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
  package="com.rnchatkitdemo">
  <uses-permission android:name="android.permission.INTERNET" />
  <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
  ...
</manifest>
```

6.  Update `.env` file with your Chatkit credentials.

7.  Set up the server:

```
cd server
npm install
```

8.  Update the `server/.env` file with your Chatkit credentials.

9.  Run the server:

```
yarn start
```

10. Update the `src/screens/Login.js`, `src/screens/Group.js`, and `src/screens/Chat.js` file with your ngrok https URL.

11.  Run ngrok:

```
./ngrok http 5000
```

12. Run the app:

```
react-native run-android
react-native run-ios
```

13. Log in to the app on two separate devices (or emulator).

## Built With

-   [React Native](http://facebook.github.io/react-native/)
-   [Chatkit](https://pusher.com/chatkit)
