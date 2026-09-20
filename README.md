# Acorn Assault

A standalone browser physics game. The playable build is `AcornAssault.html`.

## Run locally

Open `AcornAssault.html` in a modern browser. No install or server is required for the offline prototype.

## Publish on GitHub Pages

GitHub Pages is free for a public repository.

1. Push `AcornAssault.html`, `index.html`, and this `README.md` to the `main` branch.
2. Open your repository on GitHub.
3. Click **Settings** in the repository menu.
4. Click **Pages** in the left sidebar.
5. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
6. Select branch `main` and folder `/ (root)`, then click **Save**.
7. Wait one to five minutes and return to **Settings > Pages**.
8. Look for the message **Your site is live at** followed by a link. Click that link.

The URL normally follows this pattern:

`https://YOUR_GITHUB_USERNAME.github.io/YOUR_REPOSITORY_NAME/`

For example, if the username is `rajdaxini` and the repository is `AcornAssault`, the URL is:

`https://rajdaxini.github.io/AcornAssault/`

Because the repository contains `index.html`, that URL opens the game automatically. You can also open
`/AcornAssault.html` at the end of the URL, but that should not be necessary.

### If the page shows 404

- Confirm the repository is **Public**.
- Confirm `index.html` is on the `main` branch at the repository root, not inside another folder.
- Confirm Pages is using branch `main` and folder `/ (root)`.
- Wait a few more minutes after the first deployment.
- Open the Pages link from **Settings > Pages** instead of typing it manually.
- Use a hard refresh with `Ctrl+F5` if an old error is cached.

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
