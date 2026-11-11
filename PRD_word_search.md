# Product Requirements Document: Word Search

## 1. Product summary

Create a standalone, browser-playable Word Search game as `word-search.html`. Players find themed words hidden in a letter grid by selecting a straight line of letters. The game must work by opening the HTML file directly, without installing software, a server, network access, or external dependencies.

## 2. Goals

- Deliver a familiar, easy-to-understand word search suitable for casual play.
- Support mouse, touch, and keyboard selection.
- Offer a choice of themes and two puzzle sizes.
- Clearly show found words and completion progress.
- Keep all game code, styles, and content in one HTML file.

## 3. Target users

Casual players, including children and families, who want a quick word puzzle they can play in a desktop or mobile browser.

## 4. Core experience

1. Open `word-search.html`.
2. Choose a word theme and puzzle size.
3. Find the listed words in the letter grid. Words may run horizontally, vertically, or diagonally, forwards or backwards.
4. Select a word by dragging across its first and last letters, or by selecting the endpoints. Keyboard users focus a cell, start a selection, and use arrow keys to reach the endpoint.
5. Found words are highlighted and crossed off the list. Find every word to complete the puzzle.
6. Start a new puzzle at any time.

## 5. Requirements

### Functional

- **FR-1 — Standalone:** Include HTML, CSS, puzzle data, and JavaScript in one file. Use no external dependencies or network requests.
- **FR-2 — Themes:** Provide Animals, Nature, and Space word lists.
- **FR-3 — Difficulty:** Provide an Easy 10x10 grid with 8 words and a Challenge 12x12 grid with 12 words.
- **FR-4 — Puzzle generation:** Randomly place every target word in a straight line in any of the eight compass directions. Fill remaining cells with random uppercase letters. A generated puzzle must contain every displayed target word.
- **FR-5 — Selection:** Support drag selection with mouse and touch, click-to-select endpoints, and keyboard selection. Only straight horizontal, vertical, or diagonal lines are valid.
- **FR-6 — Matching:** Accept a listed word when selected forwards or backwards. Ignore words already found and highlight all cells in a found word.
- **FR-7 — Progress:** Show the target list, found/total count, elapsed time, and an announced completion state. Start the timer on the first selection and stop it when all words are found.
- **FR-8 — New puzzle:** Allow the player to generate a fresh puzzle. Changing theme or difficulty starts a fresh puzzle.

### Accessibility and usability

- Use semantic headings, buttons, labels, and a named grid.
- Make every letter cell keyboard-focusable through roving focus; arrow keys move between cells.
- Enter or Space starts a keyboard selection and finishes it; Escape cancels it.
- Provide visible focus, selected-path, and found-word styling that is not conveyed by color alone.
- Announce selection feedback, progress, and completion with a polite live region.
- Adapt the board to narrow screens without horizontal page overflow.

## 6. Out of scope

- Multiplayer, accounts, online leaderboards, and saved history.
- User-authored word lists, hints, sound effects, and network features.
- Changing or extending the existing Memory game.

## 7. Acceptance criteria

1. `word-search.html` opens and plays directly in a modern browser while offline.
2. Every theme and difficulty generates the expected grid dimensions and number of words.
3. Each displayed word can be selected in all supported directions, including backwards.
4. Invalid, bent, and unrelated selections do not count as found words.
5. Found words are visibly highlighted and crossed off; progress updates once per word.
6. The timer starts on first selection and stops on puzzle completion.
7. New puzzle, theme changes, and difficulty changes reset board, progress, and timer.
8. Keyboard-only play can reach cells, navigate the grid, select a word, and cancel a selection.
9. Touch users can drag-select without the page scrolling in response to the gesture on the board.
10. The board remains usable on a narrow phone-sized viewport.

## 8. Verification checklist

- Open the HTML directly in a browser and inspect all three themes and both difficulties.
- Select words horizontally, vertically, diagonally, and backwards; try an invalid bent selection.
- Test mouse drag, touch-style pointer interaction, and keyboard-only operation.
- Complete a puzzle and check the count, timer, and completion message.
- Generate a new puzzle and change each setting; verify reset behavior.
- Check a narrow viewport and confirm the page has no horizontal overflow.
