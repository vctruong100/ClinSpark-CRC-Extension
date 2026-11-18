# ClinSpark CRC Automator

This Manifest V3 Chrome extension packages the CRC automator for authorized
ClinSpark test-site workflows. The content script runs only on
`https://cenexeltest.clinspark.com/`.

## Included files

- `manifest.json`: extension metadata and site access declarations.
- `ClinSpark CRC Automator.js`: CRC workflow automation.
- `method-library-worker.js`: credential-free read-only Method Library request handler.
- `icons/`: Chrome extension icons.
- `PRIVACY_POLICY.md`: extension privacy policy.
- `docs/privacy-policy.html`: standalone HTML policy page for GitHub Pages.
- `NOTES.txt`: Chrome Web Store permission and publication notes.

## Local installation

1. Open Chrome and navigate to `chrome://extensions`.
2. Enable **Developer mode**.
3. Select **Load unpacked** and choose this project folder.
4. Visit an authorized ClinSpark CRC site.

## Publish the privacy policy

The policy source is `PRIVACY_POLICY.md`; the matching static web page is
`docs/privacy-policy.html`. To publish it with GitHub Pages:

1. Push these files to the repository's `main` branch.
2. In GitHub, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select
   `main` and `/docs`, then click **Save**.
4. Wait for GitHub Pages to finish deploying, then verify the page opens
   publicly at:
   `https://vctruong100.github.io/ClinSpark-CRC-Extension/privacy-policy.html`
5. Enter that URL in the Chrome Web Store listing's privacy policy field.

## Chrome Web Store release

The upload artifact is `release/ClinSpark CRC Automator 1.0.0.zip`. It contains
only the manifest, runtime scripts, and icons required by Chrome. Before each
subsequent upload to the same store listing, increment `version` in
`manifest.json`, regenerate the ZIP, and submit it for review.

## Site access

The extension injects its content script on the ClinSpark test site. It also
requests access to the production ClinSpark host for CRC features that read
production library data, and to the ACT Method Library endpoint. Requests to
ACT are anonymous, credential-free GETs and return method-library entries only.
No broad host patterns are used.
