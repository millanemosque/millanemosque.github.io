# Mill Lane Prayer Times app

A free, installable phone app (a "Progressive Web App") for Android and iPhone.
You don't need the App Store or Google Play, and there are no fees. It's hosted free on GitHub Pages.

## What's in it
- **index.html**: the app. It shows a next-jama'at countdown, this weekend's times, the rest of the month, live sunset times for Maghrib, directions, call and WhatsApp buttons, and bank details with copy buttons.
- **admin.html**: your monthly update page. Nobody can publish from it without your GitHub token.
- **times.json**: the timetable data. November 2026 is already filled in.
- **sw.js, manifest.webmanifest, icons/**: these let people install the app and use it offline.

## One-time setup (about 10 minutes, free)
1. Create a free account at https://github.com.
2. Click **+ → New repository**. Name it `mill-lane-prayer`, set it to **Public**, and click **Create**.
3. Click **uploading an existing file** and drag in *everything inside this folder*, including the `icons` folder. Then click **Commit changes**.
4. Go to **Settings → Pages**. Under "Branch" choose **main** and **/ (root)**, then click **Save**.
5. After about a minute, the app is live at `https://YOUR-USERNAME.github.io/mill-lane-prayer/`.

## Let the admin page publish (one time)
1. On GitHub, go to **profile picture → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Set these options:
   - **Repository access:** Only select repositories → `mill-lane-prayer`
   - **Permissions → Contents:** Read and write
   - **Expiration:** up to 1 year. Set a reminder to renew it.
3. Copy the token.
4. Open `https://YOUR-USERNAME.github.io/mill-lane-prayer/admin.html` on your phone.
5. Open **GitHub settings** at the bottom, paste the token, and tap **Save settings**. Your username and repository fill in automatically.

The token is saved only on that phone. Don't share it.

## Every month (about 2 minutes)
1. Open **admin.html**.
2. Pick the month and tap **Create weekends**. This adds every Friday, Saturday and Sunday with Jumu'ah 12:30 & 13:00, Zuhr 13:00 and Maghrib "After Sunset".
3. Type in Asr and Isha for each Friday. Saturday and Sunday copy them automatically.
   - Shortcut: copy the text from the WhatsApp photo (iPhone Live Text or Google Lens), paste it into the shortcut box, and tap **Read**. Then check the times.
4. Optionally, add an announcement (for example Eid times) or an extra day.
5. Tap **Publish to app**. Everyone's app updates within a minute or two.

## Share with the community
Post the link in the WhatsApp group with these instructions:
- **iPhone:** open the link in Safari → Share → **Add to Home Screen**
- **Android:** open the link in Chrome → **Install app**, or ⋮ → **Add to Home screen**

## Notes
- Maghrib is calculated as the sunset time for Mill Lane, rounded up to the next minute.
- You can change the address, phone, bank details or location at the top of `common.js`.
- If you later want a real store listing: Google Play costs a one-off $25, and you can wrap this same app with https://www.pwabuilder.com. The Apple App Store costs $99 a year.
