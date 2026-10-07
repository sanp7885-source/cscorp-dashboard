# CS Corp Business Suite

Single-page business app (quotations, invoices, projects, agreements, ledgers, cost control).
Everything is in **`index.html`** — there is no server and no database in this repo.

## 1. Put it on GitHub and open it from anywhere (free)
1. Create a free account at github.com → **New repository** → name it e.g. `cs-business-suite` (Public).
2. **Add file → Upload files** → drag in everything from this folder (`index.html`, `manifest.webmanifest`, `sw.js`, the two icons, `.nojekyll`, `README.md`) → **Commit changes**.
3. **Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save.**
4. After about a minute your app is live at `https://<your-username>.github.io/cs-business-suite/`.
5. On a phone or PC open that link in Chrome / Edge → menu → **Install app / Add to Home screen**.

> The repository holds only the *program*. Your business data is **not** stored in GitHub (so a public repo is safe).

## 2. Where your data lives (and how to keep it safe)
* Data is saved in your browser's storage (IndexedDB) for that exact web address. It stays even when you update the app.
* **Never change the repository name or GitHub username** after you start — a new address is a new, empty storage. (If it ever happens: Settings → Backup → Restore.)
* Settings → **Backup**: `Download full backup` regularly (e.g. every Friday) and keep the file in Google Drive.
* **Two people (you and your wife):** install *Google Drive for desktop* on both PCs, share one Drive folder, then in Chrome/Edge open the app → Settings → Backup → **Create shared data file** (first person, save it inside the shared folder) and **Link existing data file** (second person). Both PCs now save to that one file and merge each other's changes every ~20 seconds. Phones can use the app but cannot link the file.

## 3. Updating the app later (your data is untouched)
1. Settings → Backup → **Download full backup** (safety copy).
2. Get the new `index.html` (ask Claude for changes, paste your current `index.html`, receive the updated one).
3. In your GitHub repo click `index.html` → pencil/**Upload files** → replace the file → **Commit changes**.
4. Wait ~1 minute, refresh the page (Ctrl+F5). Your data is still there because it lives in your browser, not in the file.
5. Keep a note of changes in `CHANGELOG.md` if you like; the app version shows under Settings → Help.

## 4. Files
| File | Purpose |
|---|---|
| `index.html` | the whole application |
| `manifest.webmanifest`, `icon-*.png` | lets phones/PCs install it like an app |
| `sw.js` | opens the app offline after the first visit |
| `.nojekyll` | tells GitHub Pages to serve files as they are |

Needs internet only for: Google Fonts, Excel import/export, PDF creation (loaded from CDNs), and WhatsApp.
