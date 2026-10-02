# Celeste browser edition

**[Play Celeste or Randomizer](https://a-faus.github.io/celeste-browser/)**

A standalone GitHub Pages website. It does not depend on a personal computer
or a Cloudflare tunnel. Choose the base game or Randomizer on the home page.

## Fresh saves for every player

The `public-site/` folder is the only deployed content. The game packages
contain no original player's saves, settings, private passwords, debug
symbols, logs, or backups. Each game mode uses its own browser-local OPFS
directory. Saves stay on the player's device and are not uploaded.

Return to the same URL in the same browser profile to continue. Clearing site
data, using Incognito, browser storage eviction, or changing devices can lose
progress. Export important saves using the game's folder/filesystem button.
There is no account service or automatic cross-device save synchronization.

## First launch

The first launch downloads approximately 830 MiB of game content plus the
browser runtime; Randomizer adds approximately 11 MiB. Files are verified
with SHA-256 before installation. Later launches use the installed files.
The installer never writes any save file. The game creates fresh saves while
playing. Allow roughly 1.5 GB of browser storage for each game mode.

Use current desktop Chrome or Edge with site data and service workers enabled.
The browser game requires sufficient memory and threaded WebAssembly support;
low-end or school-managed devices may not support it.

## Deployment and credits

GitHub Actions deploys only `public-site/` to Pages. A same-origin service
worker supplies the cross-origin isolation headers needed for threaded WASM.
The base game and Randomizer use isolated browser filesystems.

Celeste and its assets belong to their respective creators. Webleste is by
MercuryWorkshop and contributors. This is a community browser deployment, not
an official release. See the website's credits page for project links and
third-party notices.
