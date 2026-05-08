# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A collection of browser-based HTML5 games. Each game is a single self-contained HTML file with inline CSS and JavaScript — no build tools, no dependencies, no frameworks.

## Running Games

Serve locally and open in browser:
```bash
python3 -m http.server 8080
# Then visit http://localhost:8080/<game>.html
```

## Architecture

- **Single-file pattern**: Each game is one `.html` file containing `<style>` and `<script>` blocks
- **Rendering**: HTML5 Canvas with `requestAnimationFrame` game loops
- **Sprites**: Drawn programmatically via pixel arrays and `fillRect` — no external image assets
- **No dependencies**: Pure vanilla JS, runs directly in any modern browser

## Git Workflow

Commit and push to GitHub after every meaningful change. Never leave work uncommitted — the user relies on git history to revert if needed.

- Write concise, descriptive commit messages (what changed and why)
- Commit after each feature, fix, or logical unit of work
- Always push to `origin/main` after committing
- Git remote: `origin` → `github.com/aatumo/retro-shooter`
- Branch: `main`

## Conventions

- All game art is procedural (pixel arrays with palette indices rendered at scale)
- Dark-themed UI styling consistent across games
- Games must work by simply opening the HTML file — no server-side logic required
