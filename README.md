# Darren's Chess Room

My chess practice site. It has a coordinate drill, a blindfold mode where you play an engine by typing moves, a blunder checker for pasted PGNs, and a stats page. Everything runs in the browser. There is no server and nothing is loaded from outside this repo.

## Running it locally

Opening `index.html` straight from a folder won't load the engine, because browsers block the worker. Serve the folder instead:

    python3 -m http.server 8000

Then go to http://localhost:8000.

## What's here

- `index.html` is the whole site.
- `chess.js` handles move rules and PGN parsing (chess.js 0.10.3).
- `stockfish.js` and `stockfish.wasm` are the engine (Stockfish.js 10.0.2). If they don't load, the site uses a weaker search I wrote, and the badge on the blunder page says so.
- `fonts/Lora-VF.woff2` is the heading font.

## Saved data

Stats and settings are stored in your browser's local storage. Clearing site data erases them.

## Licenses

- Pieces: cburnett set by Colin M. L. Burnett, copied from [Lichess](https://github.com/lichess-org/lila) (GPLv2+).
- chess.js by Jeff Hlywa, BSD 2-Clause. See `licenses/chess.js-BSD.txt`.
- Stockfish.js by Nathan Rugg and contributors, GPLv3. See `licenses/stockfish.js-GPLv3.txt`.
- Lora by the Lora Project Authors, SIL OFL 1.1. See `licenses/Lora-OFL.txt`.

Since the GPL parts are bundled, the whole repo is GPLv3. See `LICENSE`.
