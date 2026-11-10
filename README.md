# Boardfest 2026

Official Boardfest 2026 information page with meals, bedrooms, house rules and **live, no-approval chore sign-ups**.

## Website

Once GitHub Pages is enabled, the website will be at:

https://jonpeterayling-cloud.github.io/boardfest-2026/

To enable it: **Repository Settings → Pages → Build and deployment → Deploy from a branch → main → / (root) → Save**.

The entire public site is contained in `index.html`, including the Boardfest artwork and Firebase browser configuration.

## Live chore sign-ups (Firebase)

Firebase project ID: `boardfest-d7749`.

The website uses anonymous Firebase Authentication and Cloud Firestore to show in real time who has claimed the available cooking and washing-up slots. Jonny's Thursday cooking and Ben's Saturday supper cooking are reserved. Only one job per attendee; members can release a claim using the same browser that made it.

Before sign-ups will work:
1. In Firebase Console → **Authentication → Sign-in method**, enable **Anonymous**.
2. In Firebase Console → **Firestore Database → Rules**, paste the contents of [firestore.rules](firestore.rules) and click **Publish**. Uploading the rules file to GitHub does **not** deploy those security rules to Firebase.
3. Confirm that Firestore Database has been created.
4. Open the Pages site on two separate devices. Claim a job, then check the name and remaining-place count update in the other browser.

The sign-up is trust-based: visitors choose their names, rather than verifying their identities. Only the device/browser with the original anonymous login can release that claim.

## Changing information

Edit `index.html` to update the food timetable, rooms, or rules. Chore slot IDs are referenced by the Firestore rules; any change to IDs must be reflected in both places.

Boardfest dates: 12–15 November 2026.
