# Evershine Construction document portal

- The whole app is the single file `index.html` (HTML, CSS and JS inline; data in Firebase Firestore).
- Publishing: the owner wants changes live without confirming each merge. After a change is
  tested and pushed to the working branch, open a pull request into `main` and merge it straight
  away, then tell the owner it is live (they refresh with Ctrl+Shift+R).
- Printed documents and PDFs (`.sheet` styles and `drawPDF`) have a fixed layout; do not change
  them unless asked.
