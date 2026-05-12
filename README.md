# fantasy-ctfd-theme

`fantasy-ctfd-theme` is a custom CTFd player-facing theme aligned with the FantasyCTF scoreboard experience at `ctf.chron0.tech`. It keeps CTFd's core challenge behavior intact while replacing visual language, typography, and layout with a shared tavern design system.

The theme is built on top of CTFd's modern core stack (Bootstrap 5, Alpine.js, Vite). Source assets live in `assets/` and compiled artifacts are emitted to `static/`. Development uses `yarn dev` for watch builds, and production builds use `yarn build`.

This repository is intended for deployment simplicity: compiled `static/` assets are committed so production hosts can deploy by git pull without requiring Node build steps on the server.
