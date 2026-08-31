# WasteTime Chat — Corrected Firebase Config

This version uses the exact Firebase config copied from Firebase Console.

Important differences from the previous broken config:
- API key capitalization/letters were different.
- measurementId was also different.
- databaseURL is now included directly inside firebaseConfig.

Before testing:
1. Firebase Authentication -> Sign-in method -> enable Email/Password.
2. Firebase Realtime Database -> Rules -> paste firebase-rules.json -> Publish.
3. Upload all four files to your GitHub repo root.
4. Wait for GitHub Pages to redeploy, then hard refresh.
