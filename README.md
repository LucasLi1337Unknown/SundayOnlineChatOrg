# WasteTime Chat — Connected Firebase Version

This version is already configured for the Firebase project `waste-time-chat`.

## Before testing

Open Firebase Console → Realtime Database → **Rules**.

Paste the contents of `firebase-rules.json`, then click **Publish**.

Then upload these files to the root of the GitHub repository:

```text
index.html
config.js
firebase-rules.json
README.md
```

Wait for GitHub Pages to deploy, then hard-refresh the site.

Test with two computers or two different browser windows.

## Expected result

Both devices should show `online` in the top-right.

When one device sends a message, it is written under:

```text
messages/
```

in Firebase Realtime Database and should appear immediately on both devices.

## Safety note

This is intentionally a tiny public test chat. It has no real accounts, identity protection, rate limiting, moderation, or anti-spam system. Do not use it for private or sensitive conversations.
