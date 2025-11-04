# ProdInsp Dashboard

Simple static Production Data Tracker.

- Single-file app: `index.html`.
- Stores entries in browser `localStorage` (key: `prodinspector_data_v1`).
- 4 processes (Production, Inspection, Dispatch, Rejection).
- 7 parts per process (per the provided list).
- Charts use Chart.js showing daily totals and cumulative trends.
- Export: CSV for all stored records.

How to use locally

1. Open `index.html` in a modern browser (double-click or serve via a local web server).
2. Select a process tab, choose date (defaults to today), enter quantities (numbers) for any parts, and click "Save".
3. Click "Download All Data (.csv)" to export all records.

Deploy to GitHub Pages (recommended for static files)

1. Create a GitHub repository (either via web UI or `gh repo create`).
2. Add remote and push the local repo (example below).

Commands to run locally (from project folder):

```powershell
# initialize repo (if not already done)
git init
git add .
git commit -m "Initial commit: ProdInsp Dashboard"
# add remote (replace URL with your repo url)
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```

3. On GitHub, go to Settings → Pages and choose the `main` branch and `/ (root)` as folder, then Save. Your site will be live at `https://<your-username>.github.io/<repo-name>/` shortly.

If you have `gh` CLI authenticated, you can create & push in one step:

```powershell
# create a public repo and push local files
gh repo create <repo-name> --public --source=. --push
```

Notes & next steps

- This app currently uses localStorage. If you want server-backed storage (Firebase, etc.) I can reintroduce it; you'll need to provide Firebase config or I can add a small backend.
- I can optionally add a `gh-pages` deployment workflow (GitHub Actions) to auto-deploy on push.
