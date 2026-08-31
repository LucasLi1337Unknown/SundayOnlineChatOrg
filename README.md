# WasteTime Chat

A deliberately tiny public live-chat experiment for GitHub Pages.

## Features

- Pick your own display name.
- Names are 1–10 printable ASCII characters, with no spaces.
- Letters, numbers, `-`, `_`, and other printable ASCII symbols are accepted.
- Every browser session receives a random chat color.
- Live messages appear for everyone connected to the same Firebase Realtime Database.
- Last 100 messages are loaded.
- Messages are limited to 500 characters.
- User text is inserted with `textContent`, not HTML, to avoid basic HTML/script injection.

## Why Firebase?

GitHub Pages only hosts static HTML/CSS/JavaScript; it does not run a normal server-side chat backend. The page therefore uses Firebase Realtime Database as the shared realtime message store.

## Files

```text
index.html
config.js
firebase-rules.json
README.md
```

## Setup

1. Create a Firebase project at the Firebase Console.
2. Add a **Web app** to that project.
3. Create a **Realtime Database**.
4. Copy your web-app configuration into `config.js`.
5. Copy your Realtime Database URL into `databaseURL` in `config.js`.
6. In Realtime Database → Rules, paste the contents of `firebase-rules.json` and publish the rules.
7. Upload these files to the root of your GitHub repository.
8. In GitHub: **Settings → Pages → Deploy from a branch → main / root**.
9. Open the GitHub Pages URL in two different browser windows/devices and chat.

## Important: this is a test chat, not a production chat

This intentionally has **no account system**. Anyone can choose any unused-looking name, impersonate another name, spam messages, or write directly to the public database if they know its endpoint.

For a real public chat, add authentication, moderation, rate limits, server-side validation, abuse reporting, and stronger database rules.

Do not use this for private or sensitive conversations.
