# Darren's Chess Room

A personal chess training site: coordinate drills, a blindfold trainer, a blunder checker for your own games, and a stats page. It runs entirely in the browser, with no server and no outside requests.

## Put it online with GitHub Pages
1. Upload every file in this folder to the top level of a GitHub repository.
2. Open **Settings > Pages**. Under "Build and deployment", choose **Deploy from a branch**, pick `main` and `/ (root)`, then save.
3. After a minute or two the site is live at `https://<your-username>.github.io/<repository-name>/`.

## Run it on your computer
Browsers block the engine when you open `index.html` directly from a folder. Serve the folder instead:

    python3 -m http.server 8000

then open http://localhost:8000.

## Files
- `index.html`: the whole site.
- `chess.js`: move rules and PGN reading (chess.js 0.10.3).
- `stockfish.js`, `stockfish.wasm`: the Stockfish engine (Stockfish.js 10.0.2). If these fail to load, the site falls back to a simpler built-in engine.

## Your data
Progress, stats and settings are saved in the visitor's own browser (local storage). Nothing is sent anywhere.

## Credits and licenses
- Chess pieces: the cburnett set by Colin M. L. Burnett, taken from [Lichess](https://github.com/lichess-org/lila) (GPLv2+).
- chess.js by Jeff Hlywa (BSD 2-Clause), see `licenses/chess.js-BSD.txt`.
- Stockfish.js by Nathan Rugg and contributors, based on Stockfish (GPLv3), see `licenses/stockfish.js-GPLv3.txt`.

Because GPL-licensed parts are included, this repository is released under the GPLv3. See `LICENSE`.
