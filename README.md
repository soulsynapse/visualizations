# Visualizations

Standalone, dynamic visualizations written as plain HTML files with embedded JavaScript and CSS.

This repository is intended to be simple to publish with GitHub Pages: every visualization should be a browser-ready `.html` file that can be opened directly or linked from a static index page.

## Visualizations

- [Bead on a rotating hoop](simulations/rotating-hoop-bead.html)

## Goals

- Keep every visualization dynamic and interactive.
- Use plain JavaScript, HTML, and CSS.
- Avoid runtime dependencies, package managers, build steps, and frameworks.
- Make each visualization self-contained in its own `.html` file.
- Keep files ready for GitHub Pages without additional setup.

## Structure

```text
.
+-- README.md
`-- simulations/
```

Place new visualizations in `simulations/` unless another top-level category becomes useful later.

## Adding A Visualization

Create a new `.html` file:

```text
simulations/my-visualization.html
```

Each file should include everything it needs:

- Markup in the HTML body.
- Styling in a `<style>` block.
- Behavior in a `<script>` block.
- No external JavaScript libraries.
- No required local build output.

Optional external assets are fine when they are small, stable, and committed to the repo, but prefer generated canvas/SVG/DOM visuals when possible.

## Local Use

Open any `.html` file directly in a browser.

For browser features that require a local server, run one from the repo root:

```powershell
python -m http.server 8000
```

Then visit:

```text
http://localhost:8000/
```

## GitHub Pages

This repo is designed so GitHub Pages can serve the files directly.

After enabling Pages in the repository settings, visualizations should be available at paths like:

```text
https://soulsynapse.github.io/visualizations/simulations/my-visualization.html
```

## Style Guidelines

- Prefer clear controls and labels over hidden keyboard-only interactions.
- Keep animation smooth and avoid unnecessary CPU/GPU work.
- Make visualizations responsive enough to work on both desktop and mobile screens.
- Include a short title or heading inside each page so shared links are understandable.
- Keep filenames lowercase and descriptive, using hyphens between words.

