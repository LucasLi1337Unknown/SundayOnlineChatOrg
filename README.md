# WasteTime Chat — Persistent Accounts

This version adds real persistent user accounts using **Firebase Authentication (Email/Password)**.

## What changed

- Register with email + password.
- Choose a permanent chat username when registering.
- Username is 1–10 printable ASCII characters, no spaces.
- A random chat color is generated once and saved with the account.
- Log in from another computer and recover the same username/color.
- Log out button.
- Only authenticated users can read/send chat messages.
- Each message stores the sender's Firebase UID.

## IMPORTANT: enable Email/Password login first

In Firebase Console:

1. Open your `waste-time-chat` project.
2. Go to **Security → Authentication**.
3. Click **Get started** if needed.
4. Open **Sign-in method**.
5. Choose **Email/Password**.
6. Enable **Email/Password**.
7. Save.

You do NOT need to enable "Email link (passwordless sign-in)".

## Update Realtime Database rules

Open:

**Realtime Database → Rules**

Replace the rules with the contents of `firebase-rules.json`, then click **Publish**.

## Upload to GitHub

Upload these four files to the repository root:

```text
index.html
config.js
firebase-rules.json
README.md
```

Wait for GitHub Pages to redeploy and hard-refresh the site.

## Test

Computer A:
1. Register an account.
2. Pick a username.
3. Send a message.
4. Log out.

Computer B:
1. Open the same GitHub Pages URL.
2. Log in with the same email/password.
3. The same username and color should return.

You can also create a different account on Computer B and chat between the two accounts.

## Important limitations

This is still a small test chat, not a production-grade social platform.

It does not yet have:
- password reset UI
- email verification
- unique username enforcement
- profile editing
- moderation/admin tools
- spam/rate limiting
- account deletion UI

Do not use it for sensitive/private conversations.
