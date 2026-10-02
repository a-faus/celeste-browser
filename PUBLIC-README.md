# Celeste browser edition

A standalone GitHub Pages website with Celeste and the browser-compatible
Randomizer. The website does not depend on a personal computer or a tunnel.

The `public-site/` folder is the only deployed content. It contains a clean
game package: no original player's saves, settings, game manifest, passwords,
cache assemblies, debug symbols, logs or private backups are included.

Both game modes use one shared browser-local OPFS save directory. Saves stay on the
player's device and are not uploaded. Close one mode before opening the other.
Existing separate saves are backed up before migration; newer conflicting files
become active. Revisit the same URL in the same browser
profile to continue. Clearing site data, private browsing, browser eviction,
or changing devices can lose progress. Export important saves with the game's
folder/filesystem interface. No cloud save or account service is provided.

The first launch downloads approximately 830 MiB of game content plus the
browser runtime; Randomizer adds approximately 11 MiB. Files are verified
using SHA-256 before installation. Installation never writes a `Saves` file.
The game generates new save files during play.

GitHub Pages' missing COOP/COEP headers are supplied by a same-origin service
worker. Current desktop Chrome or Edge, HTTPS, service workers, persistent
site storage, and sufficient memory are required. Low-end or school-managed
devices may not support this build.

Celeste and its assets belong to their respective creators. Webleste is by
MercuryWorkshop and contributors. See `public-site/credits.html` for notices.
The repository owner has represented that they have permission to publish
the game assets. This repository is not an official Celeste release and does
not grant any additional rights to third-party assets.
