# The Morning Brief — Deploy Target

Public deploy artifacts for *The Morning Brief*, published by Third Bridge Creative. This repo contains only rendered HTML; the engine that produces it lives outside this repo (local, private).

Auto-deployed to Netlify on push to `main`.

## Files

- `YYYY-MM-DD.html` — dated daily briefings
- `index.html` — archive browser
- `netlify.toml` — deploy configuration

## Publishing a new build

From the engine workspace, run `scripts/publish.sh`. That runs the engine with `--public` (omits the Ask Claude follow-up UI), copies today's output into this folder, commits, and pushes. Netlify picks up the push and deploys.
