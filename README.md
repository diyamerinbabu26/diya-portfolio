# Diya Merin Babu — Portfolio

A responsive personal portfolio built with HTML, CSS, and a little JavaScript. GitHub Actions deploys it to GitHub Pages whenever you push to `main`.

## 1. Personalize it first

Open `index.html` and replace:
- Your professional email is set to `diyamerinbabu26@gmail.com`.
- Your LinkedIn link is set to `https://linkedin.com/in/diya-merin-babu-576378267`.
- Your GitHub profile links point to `https://github.com/diyamerinbabu26`. Replace each project link with its own repository URL when available.
- Add your resume PDF to this folder and name it exactly `resume.pdf`; the Download resume link expects that filename.
- The certification entries with exact certificate names, issuers, dates, and credential links.
- Any project description or skill that does not accurately represent your work.

You can add a PDF resume by placing it in this folder (for example, `Diya_Merin_Babu_Resume.pdf`) and adding a link in the HTML.

## 2. Create a GitHub repository

1. Sign in at https://github.com/
2. Click **New repository**.
3. Name it `diya-portfolio` (or another name you like).
4. Set it to **Public** if you want a free public GitHub Pages site.
5. Create the repository. If you're uploading these existing files, don't initialize it with another README.

## 3. Put these files into the repository

### Option A — upload in the browser
1. Open your new repository.
2. Select **Add file → Upload files**.
3. Upload `index.html`, `style.css`, `script.js`, and `README.md`.
4. Also upload the `.github/workflows/deploy.yml` file. In the upload dialog, make sure the folders `.github/workflows/` are preserved. If the browser workflow makes this awkward, use Option B.
5. Commit to the `main` branch.

### Option B — use Git in PowerShell (recommended)

Extract the downloaded ZIP, then open PowerShell in the `diya-portfolio` folder. Run:

```powershell
git init
git add .
git commit -m "Create personal portfolio website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/diya-portfolio.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username. If Git says `remote origin already exists`, use `git remote set-url origin https://github.com/YOUR-USERNAME/diya-portfolio.git` instead.

## 4. Enable GitHub Pages

1. In your repository, open **Settings → Pages**.
2. Under **Build and deployment**, choose **Source: GitHub Actions**.
3. Open the **Actions** tab and watch `Deploy portfolio to GitHub Pages`.
4. When the workflow finishes successfully, open **Settings → Pages** to find your site URL. It normally looks like `https://YOUR-USERNAME.github.io/diya-portfolio/`.

The workflow automatically deploys each new commit pushed to `main`. You can also run it manually from **Actions → Deploy portfolio to GitHub Pages → Run workflow**.

## 5. Make an update later

Edit the site files, then run:

```powershell
git add .
git commit -m "Update portfolio content"
git push
```

GitHub Actions will publish the update automatically.

## Troubleshooting

- **Workflow not running:** check that `.github/workflows/deploy.yml` is committed on `main`.
- **Pages shows a 404:** confirm **Settings → Pages → Source** is set to **GitHub Actions**, then inspect the latest workflow run.
- **Workflow permission error:** check repository **Settings → Actions → General** and the repository Pages settings. The workflow declares the Pages permissions it needs.
- **CSS or JavaScript missing:** keep `style.css` and `script.js` in the same directory as `index.html`, with matching filenames.
- **Site URL:** project repositories normally publish at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`. A repository named exactly `YOUR-USERNAME.github.io` uses the root URL.

## Before sharing your portfolio

- Check the site on both phone and desktop.
- Verify every project and certification claim.
- Add screenshots or demo links where possible.
- Do not upload API keys, passwords, private datasets, or personal information you do not want public.
