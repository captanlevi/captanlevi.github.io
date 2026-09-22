# Deploying to GitHub Pages

This site is plain static HTML/CSS/JS — no build step, no dependencies. GitHub Pages
can serve it directly once it's pushed to the right repo.

## 1. Create the repo

For a **personal (user) site**, the repo must be named exactly:

```
<your-github-username>.github.io
```

e.g. if your GitHub username is `rushibabaria`, the repo must be named
`rushibabaria.github.io`. Create it on GitHub (empty, no README/license needed) at
https://github.com/new before running the commands below.

## 2. Push this folder to it

From inside this directory (`/Users/rushi/Desktop/rushi-babaria-website/`):

```bash
git init
git add index.html style.css script.js SETUP.md
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-github-username>/<your-github-username>.github.io.git
git push -u origin main
```

Replace `<your-github-username>` in both the remote URL and the repo name with your
actual GitHub username.

## 3. That's it

For a repo named `<username>.github.io`, GitHub Pages is enabled automatically and
serves straight from the `main` branch root — no extra configuration, no GitHub
Actions workflow needed. Within a minute or two the site will be live at:

```
https://<your-github-username>.github.io
```

## Updating the site later

Edit the files locally, then:

```bash
git add -A
git commit -m "Update site"
git push
```

Changes typically go live within a minute of the push.

## Optional: verify Pages is on

If it doesn't appear after a couple of minutes, check **Settings → Pages** on the repo
and confirm the source is set to "Deploy from a branch" → `main` → `/ (root)`.
