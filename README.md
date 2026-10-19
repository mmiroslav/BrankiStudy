# BrankiStudy website

A static home page, support page, and privacy policy for GitHub Pages, following the layout of the Schengen Tracker website. No build step, JavaScript, package installation, or custom domain is required.

Public details used throughout the pages:

- App: **BrankiStudy**
- Developer: **Miroslav Milivojević**
- Support and privacy contact: **miroslav.p.milivojevic@gmail.com**
- Privacy policy effective date: **19 October 2026**

## Publish on GitHub Pages

1. Create a separate public GitHub repository, for example `brankistudy-site`.
2. Upload the **contents of this folder** to the repository root: `index.html`, `support.html`, `privacy.html`, `.nojekyll`, and the entire `assets/` folder. The README can be included too. The ZIP package contains these files inside a `BrankiStudy-GitHub-Pages` folder; upload that folder’s contents, rather than the ZIP itself.
3. Open the repository’s **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Select the branch containing the uploaded files, normally **main**, choose **/(root)**, and click **Save**.
6. Wait for the deployment to finish. Open the URL GitHub displays and check the Support and Privacy links, including the contact email.

These steps follow GitHub’s [publishing source instructions](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site). GitHub Free supports Pages from public repositories.

With the example repository name, the App Store Connect fields will use:

| Field | URL |
| --- | --- |
| Support URL | `https://YOUR-USERNAME.github.io/brankistudy-site/support.html` |
| Privacy Policy URL | `https://YOUR-USERNAME.github.io/brankistudy-site/privacy.html` |
| Marketing URL, if wanted | `https://YOUR-USERNAME.github.io/brankistudy-site/` |

Replace `YOUR-USERNAME` and the repository name with your actual values. Use GitHub’s published URL as the base. All internal links and assets use relative paths, so the pages also work at a user-site root or under another repository name.

GitHub’s branch-based Pages settings accept the repository root or `/docs`, not `/website`. Upload this website folder’s contents to the separate site repository as described above. There is no need to publish the application source repository to host these pages.

## Preview locally

From this folder, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/`. Stop the server with Control-C when finished.

## Files

- `index.html`: brief app introduction with the existing BrankiStudy icon.
- `support.html`: public email contact and frequently asked questions.
- `privacy.html`: the app and website privacy policy.
- `assets/styles.css`: shared responsive styling, keyboard focus, reduced-motion support, and print styling.
- `assets/app-icon.png`: the existing app icon, copied without modification.
- `.nojekyll`: serves the static files without Jekyll processing.

## Content and maintenance

The policy and support instructions describe the current app implementation, including offline collection/media storage, manual AnkiWeb sync, website-session cookies, desktop pairing, iOS Keychain credentials, local collection backups, support email through Gmail, and GitHub Pages hosting.

Signing out retains downloaded cards and unsynced reviews. Website and sync-key sign-ins have separate controls. The deletion instructions distinguish app data, Keychain credentials, AnkiWeb data, desktop data, and backups. The pages do not claim that all study data remains on the device when online features are used.

Before publishing, confirm that the contact details and described behavior match the version you will distribute. Revisit the policy when adding a backend, analytics, advertising, another login or sync provider, automatic data collection, or different support/hosting services. Update the effective date when the practices change.

Apple requires a privacy-policy link in App Store Connect and an easily accessible policy inside the app. This package supplies the public page; add its final published URL to the app’s Settings or another suitable location before submission. The current Settings screen does not yet contain that link. See [App Review Guideline 5.1.1](https://developer.apple.com/app-store/review/guidelines/#data-collection-and-storage).
