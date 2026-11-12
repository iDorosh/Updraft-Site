# Updraft marketing website

A standalone static website for GitHub Pages. It is separate from the iOS source project and has no build step, package dependencies, analytics, external fonts, cookies, contact form, or JavaScript.

## Files

- `index.html`: marketing page and forthcoming App Store availability.
- `support.html`: contact information, flight manual, and support answers. Use this as the App Store Support URL.
- `privacy.html`: privacy policy for the app, support email, and GitHub-hosted site. Use this as the App Store Privacy Policy URL.
- `styles.css`: responsive styling with reduced-motion support.
- `assets/`: app icon, original pilot vector artwork adapted from the game's `NeonArt.swift`, and an actual in-game capture.
- `.nojekyll`: bypasses Jekyll processing.
- `404.html`: project-URL fallback page. Its `/Updraft-Site/` paths must be changed if the repository name changes.

## Local preview

From this folder:

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

Visit `http://127.0.0.1:4173/`. No installation or compilation is required.

## Published GitHub Pages site

Published from the public repository [iDorosh/Updraft-Site](https://github.com/iDorosh/Updraft-Site), using **main → /(root)**:

- Marketing: https://idorosh.github.io/Updraft-Site/
- App Store Support URL: https://idorosh.github.io/Updraft-Site/support.html
- App Store Privacy Policy URL: https://idorosh.github.io/Updraft-Site/privacy.html

Verified live on November 11, 2026. The homepage, support page, privacy page, stylesheet, gameplay image, header icon, favicon, and all three pilot SVGs returned HTTP 200 and matched the local source bytes. Desktop and mobile visual checks passed; decorative hero overflow is clipped at the section boundary.

### Updating the site

Edit only this separate website folder, then commit and push to `main`. Existing SSH authentication was used for publication without changing credentials:

```sh
git add <changed-files>
git commit -m "Describe the website update"
git push git@github.com:iDorosh/Updraft-Site.git main
```

GitHub Pages automatically deploys updates from `main`. Check the repository’s Pages deployment before relying on a newly changed URL. Do not include the separate iOS project, signing files, or App Store working files.

If the account or repository name changes, update the canonical/social URLs and the `/Updraft-Site/` paths in `404.html`. Other internal navigation and asset URLs are relative and support GitHub project Pages. Publishing this website does not submit the app to Apple.

## After the app is released

Replace the two “Coming soon” statements with the verified public App Store URL and a real download link. Do not add an inactive App Store download button while the app is unreleased.

Contact: `Ian.dorosh@outlook.com`. The review-contact phone number is intentionally not published on the site.

## Content and privacy

The app source was audited on November 11, 2026: gameplay and motion readings remain on device; there are no accounts, advertising, analytics, third-party SDKs, or in-app purchases. The privacy policy separately explains email support and GitHub hosting. Revisit it if the app or website begins collecting data or adds external services.
