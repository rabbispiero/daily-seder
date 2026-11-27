# Daily Seder (Android)

The Daily Seder app for Android. It opens daily-seder.vercel.app full screen in Chrome's engine (a Trusted Web Activity), so Google sign-in, reminders and every website update work exactly like the web app. Changes to the website show up in the app on their own; this file only needs rebuilding for a new icon, name or setting.

App id: `app.dailyseder` (can't change after the Play Store).

## How it's built
GitHub builds the app file on every change (`.github/workflows/build.yml`, source in `android/`) and puts **DailySeder.apk** on the repo's "latest" release. The signing key is made on the first build and kept in GitHub's Actions cache (a weekly run keeps it from expiring); its fingerprint goes on the release as fingerprint.txt. The website's `/.well-known/assetlinks.json` lists that key's fingerprint, which is what hides the address bar.

## Install on your phone
1. Download **DailySeder.apk** from the link.
2. Open the file. If Android asks, allow installs from Chrome (or your file app), then tap **Install**.
3. Open **Daily Seder** and sign in with Google if it asks.
4. If you had added Daily Seder to your home screen from Chrome before, you can remove that old icon.
