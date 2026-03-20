# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **static website** hosting pre-compiled Unity WebGL builds of "Crazy Marble," an educational game by Captain Coder. It is deployed via **GitHub Pages** from the `docs/` directory. There is no source code, build system, or package manager in this repository—only exported Unity WebGL artifacts and HTML wrapper pages.

## Repository Structure

- `docs/` — GitHub Pages root
  - `index.html` — Main landing page (current edition)
  - `Build/` — Current WebGL build (`.wasm`, `.framework.js`, `.loader.js`, `.data`)
  - `TemplateData/` — Shared UI assets (CSS, loading bar images, logos)
  - `<season><year>/` — Archived editions (e.g., `s2023/`, `w2024/`, `w2025/`, `w2026/`), each self-contained with its own `Build/` and `TemplateData/`
  - `<season><year>.html` — Standalone wrapper pages for each edition

## Edition Naming Convention

Editions follow the pattern `<season><year>`: `s` = Spring, `w` = Winter (e.g., `s2023`, `w2026`).

## Deployment

Manual process: Unity WebGL exports are committed directly and served by GitHub Pages. No CI/CD pipeline exists.

## Key Differences Between Editions

- **Older editions** (pre-w2026): Fixed 960x540 canvas, static fullscreen button, simple loading bar.
- **w2026 and newer**: Responsive 16:9 aspect ratio with dynamic canvas resizing, modern spinner loading animation, mobile detection.
