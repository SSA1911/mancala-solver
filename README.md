# Mancala Solver — Capture Mode (6x4)

A single-file mancala (Kalah, 6×4 board) solver and opponent with a capture-rules engine, built as a self-contained `index.html` — no dependencies, no build step. Open it in a browser and play.

## Engine

- **Search**: iterative deepening with a heuristic leaf evaluation, plus a quiescence search (`qsearch`) so tactical capture chains are resolved before evaluation.
- **Move generation**: full legality (`isHousePlayable`, extra-turn rules) and sow-path computation (`computeSowPath`) matching capture-mode Kalah rules.
- **Modes / difficulty / first move**: selectable from the UI (`modeSelect`, `difficultySelect`, `firstMoveSelect`); hover previews the landing pit via a floating arrow and animated sowing token.
- **Persistence**: game state saved in IndexedDB (`openDb`/`loadAll`), so a reload resumes where you left off.

## Run

Open `index.html` in any modern browser. No server, install, or network access required.

## Layout

```
index.html   everything: engine, UI, styles (~1.1k lines)
```
