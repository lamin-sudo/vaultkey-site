# VaultKey — site

Source of <https://lamin-sudo.github.io/vaultkey-site/>, the public page for
VaultKey for Android: overview, privacy policy, terms, support, and the APK
download.

Four static pages, one stylesheet, no build step, no JavaScript.

| File | Role |
|---|---|
| `index.html` | Overview: features, spec sheet, install steps, download button |
| `privacy.html` | Privacy policy |
| `terms.html` | Terms of service |
| `support.html` | Formspree contact form, email, FAQ |
| `assets/site.css` | Shared styles |
| `assets/logo.svg` | The shield-and-keyhole mark — same geometry as `app/src/main/res/drawable/ic_vaultkey_mark.xml` in the app |
| `VaultKey-vNN.apk` | The release APK offered for download |

## Publishing a new build

1. Build the app: `./gradlew assembleRelease` in the VaultKey source repo.
2. Copy the artifact here with its versioned name: `VaultKey-v53.apk`.
3. Update every `VaultKey-vNN.apk` link (`index.html`, `support.html`) and the
   version / build numbers in the page headers and spec sheet.
4. Push to `main` — GitHub Pages serves it within a minute or two.

Keep the mark in sync: if `ic_vaultkey_mark.xml` changes, `assets/logo.svg` and
the three inline copies in the pages change with it.

`.nojekyll` is present so Pages serves the files as they are.
