# Acorn Assault

A standalone browser physics game. The playable build is `AcornAssault.html`.

## Run locally

Open `AcornAssault.html` in a modern browser. No install or server is required for the offline prototype.

## Publish on GitHub Pages

1. Create a GitHub repository.
2. Upload `AcornAssault.html` and this `README.md`.
3. In the repository, open **Settings > Pages**.
4. Choose **Deploy from a branch**, select the default branch and root folder, then save.
5. Open the generated Pages URL and test sign-in, OTP demo mode, levels, audio, and touch controls.

## Publish on itch.io

1. Create a new HTML game project on itch.io.
2. Upload `AcornAssault.html` as the game file or ZIP it first.
3. Enable **This file will be played in the browser**.
4. Set the viewport to a responsive size and test on desktop and mobile.

## Real phone OTP

The current file uses a local demo OTP because it works offline. The displayed code is not secure and does not send SMS.

For production authentication:

1. Create a Firebase project.
2. Enable **Authentication > Sign-in method > Phone**.
3. Add the deployed GitHub Pages or itch.io domain to authorized domains.
4. Replace the local profile and demo OTP functions with Firebase Phone Auth and reCAPTCHA.
5. Store game progress by the authenticated Firebase user ID instead of only in `localStorage`.
6. Test rate limits, failed attempts, logout, and SMS costs before public release.

Do not put Firebase Admin credentials or service-account keys in this HTML file.
