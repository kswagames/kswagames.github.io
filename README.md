# KSWA Games

Static site for [kswagames.github.io](https://kswagames.github.io). It hosts the Google Play privacy policy for each KSWA Games Android app, and the AdMob `app-ads.txt` file.

GitHub Pages serves the site from the root of the `main` branch. There is no build step. The empty `.nojekyll` file publishes the files as they are, with no Jekyll processing.

## Pages

- `index.html` — apps and the contact email
- `privacy/hangman.html` — privacy policy for Hangman
- `app-ads.txt` — AdMob app-ads.txt for publisher `pub-4773645139936122`

Contact: [kswagames@gmail.com](mailto:kswagames@gmail.com)

## Add a new app

1. Copy `privacy/hangman.html` to `privacy/<app>.html`. Use a short lowercase name, for example `privacy/wordsearch.html`.
2. Edit that page: title, description, and any wording that is specific to the app. Keep the developer name (KSWA Games) and the contact email (`kswagames@gmail.com`).
3. On `index.html`, copy an `<article class="app-card">` block inside `<div class="app-list">`. Point its privacy link at the new page, and put the app name in the visually hidden part of the link.

Leave `app-ads.txt` unchanged when the new app uses this same AdMob account. Change `app-ads.txt` only if you add another ad network or a different AdMob publisher account. Each line is:

```
domain, publisher-id, DIRECT or RESELLER, certification-authority-id
```

The current line is Google's authorized-seller entry for this account.
