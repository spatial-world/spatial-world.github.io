# SpatialWorld Project Page

Project website: **https://spatialworld.github.io**

## Local Preview

```bash
cd spatialworld
python3 -m http.server 8080
```

Open: http://localhost:8080/

## Deploy to GitHub Pages

This folder is a **standalone** site ready for the `spatialworld.github.io` repository.

### First-time setup

1. On GitHub, create a repository named **`spatialworld.github.io`**
   - Under the **`spatialworld`** organization (or a user account named `spatialworld`)
   - Public, no README / no .gitignore

2. Push from this folder:

```bash
cd spatialworld
git remote add origin https://github.com/spatialworld/spatialworld.github.io.git
git push -u origin main
```

3. In the repo: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **`main`** / **`/ (root)`**

4. Wait 1–2 minutes, then visit https://spatialworld.github.io

> A commit is already prepared locally on branch `main`. You only need to create the remote repo and push.

## Optional Assets

Add framework figure when available:

```bash
pdftoppm -png -r 150 ../SpatialWorld_NeurIPS_2026/img/spatialworld_main.pdf imgs/spatialworld_main
mv imgs/spatialworld_main-1.png imgs/spatialworld_main.png
git add imgs/spatialworld_main.png && git commit -m "Add framework overview figure" && git push
```

## Structure

```
spatialworld/
├── index.html
├── css/custom.css
├── static/          # Bulma, Font Awesome (bundled for GitHub Pages)
├── imgs/            # Project figures
└── .nojekyll
```
