# Visual Forge

**Visual Forge** is a pocket-first field system for creating, transforming, explaining, sequencing, diagnosing, and repairing visual-generation prompts.

The core application remains deliberately simple: `index.html` is a complete standalone artifact with its interface, styles, tools, and runtime JavaScript inline. It requires no framework, package manager, CDN, font service, API, build step, or network connection when opened as a local file.

## Live

**GitHub Pages:** https://westkitty.github.io/visual_forge/

GitHub's native Pages branch deployment publishes the root of `main`. The same `index.html` can be downloaded and opened locally as the guaranteed zero-dependency fallback.

## Pocket App mode

The Pages build adds a small hosted-only shell around the sovereign standalone file:

- installable metadata for iPhone Home Screen use
- dedicated Visual Forge Home Screen icon
- service-worker cache so the hosted build can reopen offline after a successful visit
- live Pocket status for launch mode, connectivity, offline readiness, and share support
- iOS/Web Share handoff for Visual Forge and generated prompt blocks, with copy fallback
- update checking from Pocket Forge

These extras are progressive enhancements. If they are absent, blocked, or unsupported, `index.html` still works by itself.

### iPhone install

Open the live Pages site in Safari, then choose **Share → Add to Home Screen → Open as Web App → Add**.

After the first successful hosted visit, Visual Forge can cache its app shell for later offline reopening. For a permanently self-contained copy, keep `index.html` in Files as well.

## What is inside

- 25 routed learning and tool modes
- Prompt Lab with local presets and constraint switches
- Prompt Doctor for failure-specific repair blocks
- Shot Builder and Lighting Recipe tools
- Reference Authority Map builder
- Wonder Lab technique deck
- Recipe Reactor that forges coherent visual-direction recipes and sends them into Prompt Lab
- Pocket Forge, an iPhone-specific one-thumb workflow and live app-status panel
- separate-image anti-collage workflow
- character turnaround and dossier methodology
- style-transfer and minimal-delta editing rules
- infographic hierarchy and grounding workflow
- canon / closed-world controls
- world reconstruction
- comics, storyboards, game assets, posters, icons, product imagery, continuity QA, and repair
- local progress, display preferences, search, copy, and share controls

## Repository shape

- `index.html` — canonical standalone Visual Forge
- `manifest.webmanifest` — hosted install metadata
- `sw.js` — hosted offline cache
- `apple-touch-icon.png`, `icon-192.png`, `icon-512.png` — install icons
- `.github/workflows/quality.yml` — standalone + Pocket App release guard
- `.nojekyll` — Pages passthrough

## Release invariants

1. `index.html` must remain useful as a local file with no hosted files present.
2. Hosted assets may enhance installation, sharing, updates, and offline reopening, but may not become prerequisites for the core tool.
3. The iPhone-first route, safe-area behavior, 25-mode navigation, and prompt tools must remain intact.
