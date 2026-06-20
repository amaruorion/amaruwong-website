# Jump Quest

A simple browser platformer game built with plain HTML5 Canvas and JavaScript. No build step, no dependencies — just one file.

## Play

Open `index.html` in any web browser. Or try it live with GitHub Pages (see below).

## Controls

| Key | Action |
| --- | --- |
| `←` / `→` or `A` / `D` | Move |
| `Space` / `↑` / `W` | Jump |
| `R` | Restart level |

Collect every coin, then touch the flag to clear the level. There are 2 levels.

## How it works

The whole game lives in `index.html`:

- A `<canvas>` element is the play area.
- A game loop (`requestAnimationFrame`) runs `update()` then `draw()` each frame.
- `update()` handles input, gravity, jumping, and axis-separated collision against platforms.
- Levels are plain data objects (`LEVELS`) listing platforms, coins, and the goal flag.

## Import with GitHub Desktop

1. Unzip this folder somewhere on your computer.
2. In GitHub Desktop: **File → Add local repository**, then pick this `jump-quest` folder.
3. Click **Publish repository** to send it to GitHub.

## Auto-publish with GitHub Pages

This repo ships with `.github/workflows/deploy.yml`, wh