# Setting this up

1. **Create the special repo.** On GitHub, create a new repository with the *exact same name* as your username (e.g. if your username is `zaki-malik`, the repo must be named `zaki-malik`). GitHub turns this repo into your profile README automatically.
2. **Push these files** to that repo, keeping the folder structure as-is (`README.md`, `assets/`, `scripts/`, `.github/workflows/metrics.yml`).
3. **Fill in the placeholders in `README.md`:**
   - `YOUR_GITHUB_USERNAME` (appears twice — typing banner link, profile-view counter)
   - `YOUR_LINKEDIN_HANDLE`, `YOUR_EMAIL@gmail.com`, `YOUR_X_HANDLE`, `YOUR_INSTAGRAM_HANDLE` (remove any badge you don't want)
4. **Enable workflow permissions:** in the repo, go to Settings → Actions → General → Workflow permissions, and select "Read and write permissions." This lets the daily GitHub Action commit refreshed cards/portrait back to the repo.
5. **Push (or manually run the Action once)** from the Actions tab → "regenerate assets" → Run workflow. This will:
   - Pull your *real* GitHub stats and top languages into `assets/card-github-*.svg` (right now they're placeholders since this sandbox has no internet access).
   - Redraw the dot-matrix portrait **with the background removed**, since the workflow installs `rembg` and downloads its model — something I couldn't do in this offline session, so the portrait you see now still has the original background.
6. **Edit `assets/skills.json`** any time to update your self-rated skill radar — the workflow redraws it automatically on the next push or schedule.

That's it — after the first Action run, everything will be live and self-updating daily.
