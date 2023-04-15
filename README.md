# push_notification

A new Flutter project.

## Getting Started
### you need firebase account
`firebase login`

### activate flutter cli
`dart pub global activate flutterfire_cli`

`flutterfire configure`

### you can skip below command by flutter pub get
`flutter pub add firebase_in_app_messaging`
`flutter pub add firebase_messaging`

you have to make below file, and fill out your keys

web/firebase-messaging-sw.js
```
importScripts("https://www.gstatic.com/firebasejs/8.10.0/firebase-app.js");
importScripts("https://www.gstatic.com/firebasejs/8.10.0/firebase-messaging.js");

firebase.initializeApp({
  apiKey: "...",
  authDomain: "...",
  projectId: "...",
  storageBucket: "...",
  messagingSenderId: "...",
  appId: "...",
});

const messaging = firebase.messaging();

// Optional:
messaging.onBackgroundMessage((message) => {
  console.log("onBackgroundMessage", message);
});
```

### you can choice platform at commandline
`flutter run`
