# Halloween Championship — publish your website

This package is configured for your existing Firebase **Cloud Firestore** project, not Realtime Database. Your Firebase controller account already exists.

1. Open Firebase Authentication → Settings → Authorised domains. Add `YOUR-USERNAME.github.io` once you know your GitHub username, if it is not already listed.
2. In GitHub, create a **public** repository named `halloween-championship`. Upload `index.html`, `style.css`, `app.js`, and `config.js` to its root. Do not upload passwords.
3. Open repository Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save. Wait for the deployment URL.
4. Open `https://YOUR-USERNAME.github.io/halloween-championship/` on your phone. Tap Create a new championship, then sign in using the Firebase Authentication account you already created. Tap Create scoreboard.
5. Copy the TV link from the phone controller and open it in the Samsung TV browser. Updates on your phone appear on the TV live.

## Security
The Firestore rules you published permit anyone to read championship documents, but only the Firebase UID you authorised to write. Never store private details in the scoreboard. A public GitHub Pages repository contains the public Firebase web configuration, not your password.

## Troubleshooting
- `Permission denied`: ensure the Firestore rules refer to the same Firebase controller UID and the account is signed in.
- `auth/unauthorized-domain`: add your GitHub Pages domain to Authentication → Settings → Authorised domains.
- TV waiting: create the scoreboard on the phone first and check both devices use the same room URL.
- The Samsung browser may be too old for the Firebase JavaScript SDK; try updating firmware or using a streaming device browser.
