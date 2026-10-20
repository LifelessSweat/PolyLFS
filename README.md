# PolyTrack 0.6.3 (northstar mod) — GitHub Pages build

This folder is the whole playable game, ready to host on GitHub Pages. It talks to the leaderboard and multiplayer
server at `polytrack-leaderboard.minceraft-player-2010.workers.dev`, which accepts requests from any website.

## Put it online

1. Create a new repository on GitHub (for example `northstar`). It can be public, or private if your plan includes
   Pages for private repositories.
2. Put **the contents of this folder** at the top of the repository, including the hidden `.nojekyll` file. With
   GitHub Desktop: clone the empty repository, copy everything from this folder into it, commit, and push.
   (The GitHub website only accepts 100 files per upload, and this build has about 550, so use GitHub Desktop or git.)
3. On GitHub, open the repository's **Settings → Pages**. Under "Build and deployment", choose
   **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute or two the game is live at `https://<your-username>.github.io/<repository>/`.

## Updating it

Rebuild the game in `northstar0.6.3_work` (`npm run build`), then replace this folder's contents with the new
`dist/` folder, leaving out `dist/electron/` and `dist/package.json` (only the desktop app uses them), and push
again. Keep `.nojekyll` and this README.
