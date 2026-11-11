# Childhood Browser Games

A small collection of responsive, self-contained games built with HTML, CSS, and JavaScript. No installation, build step, external libraries, or network connection is required.

## Games

### Memory Game

Open [`memory-game.html`](./memory-game.html) in a browser to match pairs of cards.

- Play on 4x4 or 6x6 grids.
- Track moves, elapsed time, and a star rating.
- Save the five best scores in browser local storage.
- Play with a mouse or keyboard.

### Word Search

Open [`word-search.html`](./word-search.html) in a browser to find hidden words in a letter grid.

- Choose Animals, Nature, or Space word themes.
- Choose Easy (10x10, 8 words) or Challenge (12x12, 12 words).
- Find words horizontally, vertically, or diagonally, forwards or backwards.
- Select words by dragging, clicking endpoints, or using the keyboard.
- Track found words and elapsed time.

See the [Word Search PRD](./PRD_word_search.md) for its product requirements and verification checklist.

## Run locally

The simplest way to play is to open either HTML file directly in a modern browser. Alternatively, from this folder, run a local server:

```bash
python3 -m http.server 8000
```

Then open:

- `http://localhost:8000/memory-game.html`
- `http://localhost:8000/word-search.html`

## Project files

- `memory-game.html` - Memory game, including its styles and game logic.
- `word-search.html` - Word Search game, including its styles, word lists, and game logic.
- `PRD_word_search.md` - Word Search feature requirements and acceptance checklist.

Both games are standalone HTML files and require no dependencies.
