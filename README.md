# Nokia Snake

A faithful recreation of the classic Nokia 3310 Snake game — single HTML file, zero dependencies. Just open in a browser and play.

---

## Features

- **Nokia Look & Feel** — Phone-shaped frame with green LCD screen using the classic Game Boy palette (`#9bbc0f`).
- **Wall & Self Collision** — Hit a wall or your own tail and it's game over, just like the original.
- **Progressive Speed** — Starts slow; speed increases every 50 points (up to level 9).
- **High Score Tracking** — Best score persists during the session.
- **HiDPI Rendering** — Canvas renders at native `devicePixelRatio` for crisp visuals on Retina displays.
- **Zero Dependencies** — One self-contained `.html` file with embedded CSS and JavaScript.

## Controls

### Keyboard

| Key | Action |
|-----|--------|
| Arrow keys / WASD | Change direction |
| P | Pause / Resume |
| R | Reset game |
| Space | Pause (in game) / Restart (game over) |

### On-Screen

D-pad buttons (▲▼◀▶), Pause (‖), and Reset (RST) — works with both mouse click and touch.

### Touch

Swipe on the LCD screen to change direction.

## Getting Started

1. Download `SnakeGame.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).

Or serve locally:

```bash
python -m http.server 8080
# visit http://localhost:8080/SnakeGame.html
```

## Game Rules

- Snake starts at the center moving right with a length of 3.
- Eat the food square to grow and score 10 points.
- Every 50 points the speed increases by one level.
- Hitting a wall or your own body ends the game.

## Tech Notes

- **Grid:** 20 × 20 cells on an HTML5 Canvas.
- **Tick rate:** 160 ms at level 1, decreasing by 12 ms per level, minimum 60 ms.
- **Input:** Queues the next direction to prevent 180° reversals within a single tick.
- **Mobile:** `touch-action: none` and `user-select: none` prevent scroll/selection interference.

## License

MIT
