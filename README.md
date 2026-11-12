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

## Publish to GitHub Pages

1. Create the public GitHub repository `iDorosh/Updraft-Site`.
2. Commit and push only this website folder to its `main` branch. Do not include the separate iOS project, signing files, or App Store working files.
3. In the repository, open **Settings → Pages**. Select **Deploy from a branch**, `main`, and `/(root)`, then Save.
4. Wait for the Pages deployment to finish and verify all three URLs:
   - Marketing: `https://idorosh.github.io/Updraft-Site/`
   - Support: `https://idorosh.github.io/Updraft-Site/support.html`
   - Privacy: `https://idorosh.github.io/Updraft-Site/privacy.html`
5. Paste the support and privacy URLs into App Store Connect. Publishing this website does not submit the app to Apple.

If the account or repository name changes, update `404.html` and any canonical/social URLs before publishing. Other internal navigation and asset URLs are relative and support GitHub project Pages.

## After the app is released

Replace the two “Coming soon” statements with the verified public App Store URL and a real download link. Do not add an inactive App Store download button while the app is unreleased.

Contact: `Ian.dorosh@outlook.com`. The review-contact phone number is intentionally not published on the site.

## Content and privacy

The app source was audited on November 11, 2026: gameplay and motion readings remain on device; there are no accounts, advertising, analytics, third-party SDKs, or in-app purchases. The privacy policy separately explains email support and GitHub hosting. Revisit it if the app or website begins collecting data or adds external services.
