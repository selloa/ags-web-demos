# AGS Web Games

Dev test catalog for Adventure Game Studio web exports. Each subfolder is one game (`index.html`, `ags.js`, `my_game_files.js`, etc.).

## Add a game

1. Copy the full AGS web export folder into this directory (same level as `2001`, `Bernard-Test`, …).
2. Regenerate the catalog:

   ```powershell
   .\scripts\generate-catalog.ps1
   ```

The script picks up any folder that contains both `index.html` and `ags.js`, then rewrites `index.html` and `games.json` at the repo root.

## Run locally

AGS needs HTTP (not `file://`). Double-click **[serve-local.bat](serve-local.bat)** to start a server on port 8000 and open the catalog in your browser.

Or from the repo root:

```powershell
python -m http.server 8000
```

```powershell
npx --yes serve .
```

Click a title to play; use **← All games** in the header to return to the list.

## GitHub Pages (later)

1. Run `.\scripts\generate-catalog.ps1` so the root `index.html` lists all games.
2. Push the repo and enable Pages (source: root `/`).
3. Share the Pages URL.

Remove nested `.git` folders inside game directories before publishing if you do not need them.
