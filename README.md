# SpatialWorld Project Page

Project website for **SpatialWorld: Benchmarking Interactive Spatial Reasoning of Multimodal Agents in Real-World Tasks**.

Live URL (after deployment): https://spatialworld.github.io

## Local Preview

From the repository root:

```bash
cd /Users/thhd/Desktop/docs
python3 -m http.server 8080
```

Then open: http://localhost:8080/spatialworld/

## Deploy to GitHub Pages

### Option A — Dedicated repo `spatialworld.github.io` (recommended)

1. Create a GitHub repo named `spatialworld.github.io`
2. Copy the contents of this `spatialworld/` folder to the repo root (or push this whole `docs` repo and set Pages source to `/spatialworld`)
3. In **Settings → Pages**, set source to `main` branch, folder `/` (or `/spatialworld` if keeping subfolder)
4. Wait ~1–2 minutes; site will be live at https://spatialworld.github.io

### Option B — Subfolder in existing repo

1. Push this repo to GitHub
2. **Settings → Pages → Build and deployment → Folder**: select `/spatialworld`
3. Site URL: `https://<username>.github.io/<repo-name>/spatialworld/`

## Add Missing Assets

Export these figures from your LaTeX paper (`SpatialWorld_NeurIPS_2026/img/`) as PNG and place them in `imgs/`:

| File | Source |
|------|--------|
| `spatialworld_main.png` | `img/spatialworld_main.pdf` |
| `pipeline_data.png` | `img/pipeline_data.pdf` |
| `scenario_task_distribution_bar.png` | `img/scenario_task_distribution_bar.pdf` |
| `gallery/ai2thor_fp.png` | `img/figure2_ai2thor_fp.pdf` |
| `gallery/carla_fp.png` | `img/figure2_carla_fp.pdf` |
| `gallery/virtualhome_fp.png` | `img/figure2_virtualhome_fp.pdf` |

Convert PDF to PNG (macOS):

```bash
brew install poppler   # if needed
pdftoppm -png -r 150 img/spatialworld_main.pdf imgs/spatialworld_main
mv imgs/spatialworld_main-1.png imgs/spatialworld_main.png
```

## Update Links

Edit `index.html` and replace `#` placeholders in the Paper / Code / Benchmark buttons with your actual URLs.

## Structure

```
spatialworld/
├── index.html          # Main project page
├── css/custom.css      # SpatialWorld-specific styles
├── imgs/               # Figures and paper preview
└── README.md           # This file
```

Shared static assets (Bulma, Font Awesome) are loaded from `../static/` in the parent repo.
