# Catch the Memory

A single-file memory card game (`catch-the-memory.html`). No libraries or assets: open it in a browser and play.

## How to play
1. Pick a **mode**: Easy (2 min), Medium (1 min) or Hard (30 s).
2. Pick a **topic**: Food and Drinks, Animals, Vehicles and Transportation, Nature and Weather, Sports and Hobbies, Space and Astronomy, Clothing and Accessories, or Shapes and Colors.
3. Flip two cards at a time on the 4×6 board (24 cards, 12 pairs). Match all pairs before time runs out, or you lose.

The timer starts on your first flip. The last 10 seconds beep and flicker. **Topics** during a game asks to confirm forfeiting and pauses the clock. 🔊 mutes the sound.

## Key functions
| Function | What it does |
|---|---|
| `startGame()` | Builds and shuffles the deck for the chosen mode and topic, and resets the state. |
| `onFlip(i)` | Handles a card click: flips it, checks for a match or mismatch, and updates the score. |
| `startTimer()` / `tick()` | Run the countdown, play the beeps for the last 10 seconds, and end the game at 0. |
| `pauseGame()` / `resumeGame()` | Freeze and restart the clock while the forfeit box is open. |
| `askForfeit()` | Shows the Yes/No forfeit box when **Topics** is pressed mid-game. |
| `endGame(win)` / `showResult(win)` | Stop the game, play the win or lose sound, reveal missed cards, and show the result screen. |
| `sfx` | Sound effects made with the Web Audio API: `flip`, `match`, `miss`, `win`, `lose`, `tick`. |
| `shuffle(a)` | Fisher-Yates shuffle. |

## Customizing
- **Modes and times:** edit the `MODES` object.
- **Topics and items:** edit the `TOPICS` array. Each item is `[name, emoji]` or `[name, "svg:key"]` for a custom icon in `SVG`.
