STUDY TRACKER — PIRATE VOYAGE EDITION

FILES
- study-tracker-v5.html: the updated tracker app
- study-tracker.webmanifest: install metadata
- study-tracker-sw.js: offline app-shell cache
- study-tracker-icon.svg: original vector pirate-adventure icon

NORMAL USE
Open study-tracker-v5.html as before. Your existing app storage keys and study data logic were not intentionally changed. The theme preference uses a separate key named study-tracker-theme.

PWA INSTALL + OFFLINE
Progressive Web App installation and service workers require HTTPS or localhost; they do not work when the HTML is opened directly using file://. Put all four files in the same folder on a static HTTPS host, or serve the folder from localhost. Then open study-tracker-v5.html in Android Chrome and use the Install button/browser menu when offered. Open the app once online so the app shell can be cached for offline use.

DATA MIGRATION NOTE
Browser localStorage is scoped to the browser origin/profile. If you move from a local file to an HTTPS-hosted version, the hosted origin will have separate storage. Export a JSON backup from the existing tracker before moving, then import it into the hosted version. Keep the original file and backup until you have verified the imported data.

PRIVACY
The app shell is cached locally. No analytics or third-party tracking was added. Study records remain in the app's existing browser storage; they are not uploaded by the service worker.
