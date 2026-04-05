# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static HTML/CSS/JS website for DanD Landscape Services, deployed to GitHub Pages via the `gh` CLI.

## Deployment

The site is deployed to GitHub Pages. To deploy:

```bash
# If the repo doesn't exist yet, create it and push
gh repo create dandlandscapeservices --public --source=. --push

# Enable GitHub Pages (run once, targeting the main branch root)
gh api repos/:owner/dandlandscaping/pages -X POST -f source[branch]=main -f source[path]=/

# For subsequent deploys, just push to main
git add .
git commit -m "your message"
git push
```

The live site URL will be: `https://<username>.github.io/dandlandscaping/`

## Structure

This is a static site — no build step, no package manager, no framework. Files are served as-is from the repo root (or a `/docs` folder if GitHub Pages is configured that way).
