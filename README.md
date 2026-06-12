# ZigQuest — web builds

Public, auto-deployed builds of **ZigQuest** — a Terraria-inspired 2D pixel-art game where you
learn the Zig programming language by writing code that changes the game world. Runs entirely in
the browser: no build step, no frameworks, no dependencies.

### ▶ Play & track progress
**https://noelruault.github.io/zigquest-web/**

## What this repo is

This repo holds only the **built, minified game bundle**, published automatically. The source code
lives in a separate **private** repository and is developed by an autonomous "improvement loop" that
lands one polished mechanic per iteration.

The site serves a new version on every iteration:

- **`/dev`** — latest in-flight build (refreshes each loop iteration)
- **`/stable`** — latest milestone-approved build (updates when a milestone is merged)
- **`/snap/<commit>/`** — a frozen, playable build for every version (browsable history)

…plus a mobile-friendly picker at the root showing milestone progress and the full version list.

## How it's published

A CI job in the private source repo bundles the game with `esbuild` into a single `game.min.js`,
pairs it with the HTML/CSS shell, and pushes the result to this repo's `gh-pages` branch on every
version. **No source modules, docs, tests, or build tooling are published here** — only the playable
bundle.

> Note: this is a client-side game, so the minified JavaScript still runs in your browser. Bundling
> removes the source structure, comments, and internal docs — it is not obfuscation or encryption.

## Status

Auto-generated build artifacts. Contact the owner ([@noelruault](https://github.com/noelruault)) for
licensing or questions.
