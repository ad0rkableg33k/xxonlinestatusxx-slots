# xXOnlineStatusXx SLOTS

## Project Overview
Single-file browser slot machine game hosted on GitHub Pages.
Everything — HTML, CSS, and JS — lives entirely in index.html.
No build step. No dependencies. No package.json.

## Stack
- Vanilla HTML/CSS/JS only
- Google Fonts: Orbitron + Share Tech Mono (loaded via @import)
- GitHub Pages static hosting
- Zero frameworks, zero npm, zero bundler

## Structure
- index.html — the ENTIRE project (1600+ lines)

## Architecture
- Three slot machine games: BabyyBat, Drag0n, and Iconic (classic)
- Character select landing screen
- Shared wallet/coin system across all three games
- Mini-games/bonus rounds triggered by BAR symbols
- Particle effects system
- Starfield canvas background
- CSS variables for theming: --pink, --magenta, --cyan, --gold
- Each machine has its own reel logic, pay tables, and highlight system

## Key Functions
- batSpin() / dragSpin() / iconSpin() — main spin handlers
- evalLine243() — shared win evaluation
- hlCells() / clearAllHighlights() — reel highlight helpers
- openMiniGame() — bonus round handler
- spawnParticles() — particle system
- updateWallet() — shared coin display

## CSS Architecture
- CSS variables on :root for all colors and glows
- .screen / .screen.active — screen switching system
- .machine.bat-machine / .dragon-machine / .iconic-machine — per-character theming
- .reel-strip — positioned absolutely, animated via JS top value

## Conventions
- KEEP EVERYTHING in index.html — do not split into separate files
- Do NOT introduce npm, node_modules, or any build tools
- Do NOT add frameworks (no React, Vue, etc.)
- Maintain the dark neon aesthetic: deep purple/black background, pink/magenta/cyan neon glows
- All new symbols must be emoji
- Coin system is localStorage-based (persists between sessions)

## Deployment
Push to main → auto-deploys via GitHub Pages. No build step needed.
