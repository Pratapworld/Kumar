# How to Publish This Site on GitHub Pages

Your website address will be: **https://YOURUSERNAME.github.io**
(Replace YOURUSERNAME with your real GitHub username, all lowercase.)

---

## Step 1 — Get a GitHub account
- Go to https://github.com and sign up (free) if you don't have an account.
- Note your **username** — it becomes part of your website address.

## Step 2 — Create the repository
1. Click the **+** button (top-right) → **New repository**.
2. Repository name: type exactly `YOURUSERNAME.github.io`
   - Example: if your username is `pratapkumar`, name it `pratapkumar.github.io`.
   - This exact name is what turns the repo into a website.
3. Choose **Public**.
4. Do NOT add a README. Click **Create repository**.

## Step 3 — Upload the files (read carefully)
1. On the new empty repo page, click the link **"uploading an existing file"**.
2. On your computer, open the `grid-engineer-site` folder.
3. Select **everything INSIDE it**:
   - Files: `index.html`, `about.html`, `style.css`, `script.js`
   - Folders: `notes`, `calculators`, `updates`, `bihar-tracker`, `ai-for-engineers`
4. Drag all of them into the GitHub upload box.

   ⚠️ Upload the **contents**, not the `grid-engineer-site` folder itself.
   `index.html` must be at the top (root) of the repository, or the site won't open.
5. Scroll down and click **Commit changes**.

## Step 4 — Turn on GitHub Pages
1. In the repo, open **Settings** (top menu) → **Pages** (left menu).
2. Under "Build and deployment" → **Source**: choose **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)** → click **Save**.

## Step 5 — Open your live site
- Wait 1–2 minutes.
- Visit: **https://YOURUSERNAME.github.io**
- Done!

---

## Updating the site later
- **Add an update/photo:** edit `updates/updates.json`, add a new block at the top, commit.
  Put photos in `assets/images/` and set the `"image"` field to `../assets/images/yourphoto.jpg`.
- **Add a note:** create a new `.html` page in the `notes/` folder and link it from `notes/index.html`.
- Every change you "commit" on GitHub goes live automatically in 1–2 minutes.

## Optional: custom domain later
- Buy a domain like `pratapgrid.com`.
- In **Settings → Pages → Custom domain**, enter it and follow the DNS steps.
