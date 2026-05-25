# tap-dungeon-crawler

A **top-down, web-based, mobile-focused roguelike dungeon crawler** with **tap controls**.

## Initial work plan (do this first, in order)

1. **Bootstrap the GitHub repo from the start** — *before* any prototype code:
   - Create a **public** repo on this VM's dedicated account `sandbox-vm-kenyon` (see `~/Documents/agent-vm-control-reference/github-account.md` for the active classic PAT and CLI usage).
   - Repo name: `tap-dungeon-crawler` (match this project folder).
   - **Add collaborator `randyhaylor` immediately.**
   - Initialize with a README.md (one-paragraph description) and a `.gitignore` for web/node.
   - First commit + push from this project folder. Don't dump everything later; commit small, working steps as you go.
2. **Build a playable prototype** with **rudimentary graphics** — function over polish:
   - Top-down view, mobile-first responsive layout, **tap controls** are primary.
   - Roguelike fundamentals first: a tile grid, procedurally generated dungeon room/corridor, a player avatar, simple enemies, basic combat, line-of-sight or fog-of-war, a turn loop, death + restart.
   - Pick the simplest stack that runs in a browser with no build step needed for testing (e.g., a single static HTML/CSS/JS file is fine for v0). You may use a tiny canvas/2D framework if it saves time, but avoid heavy engines until the prototype shows the core loop works.
   - "Rudimentary graphics": colored rectangles / Unicode glyphs / minimal sprites are fine — playability over aesthetics.
3. **Host it with ngrok** so it can be opened from a phone for live testing:
   - Serve the static files locally (Python's `http.server` or similar is fine).
   - `ngrok http <port>` to get a public URL. (See `~/Documents/agent-vm-control-reference/ngrok.md` if present.)
   - Confirm the URL loads on a phone and tap controls work.

## Constraints

- This project lives inside the VM sandbox at `~/sandbox-projects/tap-dungeon-crawler/`.
- The git identity for commits should be the dedicated account `sandbox-vm-kenyon` (configure `git config user.name` / `user.email` accordingly for this repo; do not push as the host user).
- Stay mobile-first: every interaction must work via single-finger taps. Keyboard support is optional bonus, not the design target.
- Keep dependencies minimal and pinned. Prefer browser-native APIs.

## Workflow notes

- You are running inside a Claude Code session named `tap-dungeon-crawler` with Remote Control enabled, so the user may steer you from a phone app at any time.
- When you finish a meaningful unit of work (repo created, prototype walkable, prototype playable, ngrok URL live), surface a one-line summary so the user knows where you are.
- The host user's host-side agent stands by; it can move files in/out of the VM or run host-side tasks on request — ask the host if you need something outside the VM's reach.
