# SpatialWorld Project Page

Live website: https://spatial-world.github.io/

This static site presents SpatialWorld's published paper, benchmark,
annotated task examples, evaluation protocol, reported results, and ablations.
The result tables and figures follow arXiv v2 (13 June 2026):
https://arxiv.org/abs/2606.09669v2

## Local preview

```sh
python -m http.server 8080
```

Open http://localhost:8080/ from this repository's root.

## Update and publish

- Edit `index.html` and `css/custom.css`.
- Place paper figures and task screenshots under `imgs/figures/`.
- Verify figure sources, table values, links, and responsive layout.
- Push the reviewed changes to the `main` branch of
  `https://github.com/spatial-world/spatial-world.github.io.git`.
- GitHub Pages publishes the repository root. Check the live site after deployment.

Keep numerical claims tied to their publication or evaluation version.
The paper's reported results are not a live leaderboard.
