# Privacy Policy for ClinSpark CRC Automator

Effective date: November 18, 2026

ClinSpark CRC Automator runs workflow automation in the user's browser on the
authorized ClinSpark CRC environment.

The extension injects its content script only on
`https://cenexeltest.clinspark.com/`. It also has host access to
`https://cenexel.clinspark.com/` for CRC features that read production library
data and to `https://act-master-schedule.onrender.com/` for the Method Library.

## Data handling

The extension does not collect, sell, or share user data with the developer.
Its content script interacts with ClinSpark pages using the user's active
browser session. ClinSpark requests and records are handled by the ClinSpark
application, not sent to the extension developer.

The Method Library feature makes an anonymous, credential-free GET request to
the ACT Master Schedule Method Library endpoint. The request does not include
ClinSpark page data, account identifiers, or authentication cookies. The
response contains method names, categories, and expressions only.

## Storage

Automation state and interface preferences may be stored locally in the
browser's site storage. The extension does not transmit this local storage to
the developer.

## Remote code

The extension does not download or execute remote code. Extension code is
included in the package and updates are distributed through the Chrome Web
Store.

## Contact

For questions, contact the extension owner or administrator responsible for
the Chrome Web Store listing.
