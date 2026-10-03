# Evershine Construction document portal

- The whole app is the single file `index.html` (HTML, CSS and JS inline; data in Firebase Firestore).
- Publishing: the owner wants changes live without confirming each merge. After a change is
  tested and pushed to the working branch, open a pull request into `main` and merge it straight
  away, then tell the owner it is live (they refresh with Ctrl+Shift+R).
- Printed documents and PDFs (`.sheet` styles and `drawPDF`) have a fixed layout; do not change
  them unless asked.
- Access: roles owner / staff / viewer. Team members live in the Firestore `team` collection
  (doc id = lowercase email); the main owner email is hard-coded as OWNER_EMAIL. The server-side
  limits are the Firestore rules in `firestore.rules` (same text as FIRESTORE_RULES in index.html,
  shown in Settings → Team). Keep the two in sync; the owner pastes them into the Firebase console.
- Data: Firestore collections `docs`, `customers`, `expenses` (owner/staff only), `places` (custom trip places for the island picker), `team`, and `settings/company`
  (products and signature live in settings). Any new collection needs a matching rule in FIRESTORE_RULES.
