# Dash Run

A simple browser platformer built with plain HTML5 Canvas and JavaScript. No build step, no dependencies — just one file (`index.html`). Lives at [amaruwong.com](https://amaruwong.com).

## Play

Open `index.html` in any web browser.

## Controls

| Key | Action |
| --- | --- |
| `←` / `→` or `A` / `D` | Move |
| `Space` / `↑` / `W` | Jump |
| `Shift` / `X` | Dash |
| `R` | Restart room |

Dash and jump across obstacles to traverse each room. Spikes and pits send you back to the start of the current room. The rooms flow into each other left to right — walk off the right edge of one and you enter the next from the left. Reach the flag in the final room to win. There are 6 rooms.

## How it works

The whole game lives in `index.html`:

- A `<canvas>` element is the play area.
- A game loop (`requestAnimationFrame`) runs `update()` then `draw()` each frame.
- `update()` handles input, gravity, jumping, a short dash, and axis-separated (sub-stepped) collision against platforms.
- Rooms are plain data objects (`ROOMS`) listing platforms, spikes, and the goal flag. Walking off the right edge advances to the next room; falling in a pit or touching a spike respawns you at the room start.

## Auto-publish with GitHub Pages

This repo ships with `.github/workflows/deploy.yml`, which builds and publishes the site to GitHub Pages automatically on every push to `main`. The `CNAME` file points the site at `amaruwong.com`.

To update the live game: edit the files, then commit and push (GitHub Desktop or `git push`). The workflow redeploys within a minute or two.

## License

MIT — see [LICENSE](LICENSE).
