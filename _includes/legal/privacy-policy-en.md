# Prime Attack Privacy Policy

Effective: 24 October 2026

Prime Attack ("the app") has no accounts and collects no information that identifies you — no name, email, phone number, address, contacts or photos. It shows no ads, uses no advertising identifier, and sells no data.

What follows is everything the app handles.

## 1. Stays on your device

- **Play log**: for each round, the number of balls cleared, shots taken, whether you cleared it, the score and the stage are written to a file on the device. The file never leaves the device and is removed when you uninstall the app.
- **Sound and vibration settings**: kept only while the app is running; nothing is saved.

## 2. Crash reports (Google Firebase Crashlytics)

When the app stops unexpectedly or hits an error, a report is sent so the cause can be found. It contains where the error happened (a stack trace), the app version, the device model and OS version, and an installation identifier (a random value that changes if you reinstall). It contains no name or contact details.

## 3. Usage analytics (Google Firebase Analytics)

To see where the game gets hard, the app sends these five events and nothing else of its own.

| Event | Values sent with it |
|---|---|
| Stage start | stage number |
| Stage clear | stage number, shots, stars, score |
| Stage fail | stage number, balls left |
| Hint used | stage number, the ball's number |
| Run end | last stage, total score |

Separately, the Firebase SDK records basic events such as first open and session start. Analytics also uses an app instance identifier (a random value that disappears when you uninstall), device model, operating system, language, and an approximate region that Google derives from the IP address; the app does not store IP addresses.

## 4. Leaderboard (Apple Game Center / Google Play Games)

The leaderboard works only if you are signed in to the platform. If you are, your cumulative score is submitted when a run ends in failure. The score and player name are held by the platform, not by the app. If you are not signed in, nothing is submitted and the game plays normally.

## 5. Purpose and retention

This data is used only to fix errors and tune difficulty. Crash and analytics data are kept under Google's retention policies (Crashlytics up to 90 days, Analytics up to 14 months) and then deleted.

## 6. Processors

- Google (Firebase Crashlytics, Firebase Analytics) — <https://firebase.google.com/support/privacy>
- Google (Play Games Services) and Apple (Game Center) — each under its own privacy policy

## 7. Stopping collection

Uninstalling the app removes the on-device log and stops any further data being sent. Signing out of the platform account stops leaderboard submissions.

## 8. Children

The app is not directed at children, and no data is knowingly collected from them.

## 9. Your rights

To ask what was sent or to have it deleted, write to the address below. Because no identifying information is collected, the app instance identifier from your device may be needed to locate your records.

## 10. Changes

If this policy changes, the effective date above is updated and the change ships with a new app version.

## 11. Contact

uaremine@gmail.com
