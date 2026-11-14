# Brought in: magnet-crew

- From: the Magnet Crew claude.ai artifact (https://claude.ai/artifact/FGWKWWBFUkgop8oQRWboGz), saved as index.html, 2026-11-14
- Baseline: the tag `baseline/magnet-crew`, holding only the game's files as they came in
- The original was not changed. Its history, if it had one, stays with it.

| File | Bytes | SHA-256 |
|---|---|---|
| `index.html` | 26079 | `d40c01e520d7a3c209754815040541e95d7912237314966381b20f59e62ddb57` |

## Read from the game

- Read: `index.html` whole (419-line inline script plus markup and CSS).
- Where each `[x]` lives:
  - 60 s shift, timer, HUD: `index.html:109` (`SHIFT`), `hud()`; start.png, play-10s.png
  - Streaming bots onto a held part: `sendOne` `index.html:147`, hold loop ~`:205`, `pointerdown` `:447`; play-10s.png
  - Lift when clamped bots ≥ weight, float to furnace: `:226`; overcharge speed `:229`
  - Cells build bots / scrap pays credits: `smelt` `:170`
  - Pulse recall: `pulse` `:159`
  - Part spawning scales with crew: `:217`-`:219`
  - Start and end cards, best score in localStorage (`magnetcrew-best`): `:469`-`:473`; first.png, end.png
  - Haptics: `buzz` `:193`
- Tuning values: `SHIFT 60`, `ROLL 125`, `FLOAT 52`, `STREAM_EVERY 0.085` (`:109`); spawn interval 3.2 s, max 9 parts, max weight `min(25, 0.8 × bots)` (`:217`-`:219`); scrap value `round(w·10·(1+w/8))`, cell build `max(2, round(1.6·w))`; overcharge cap 2× weight.
- Counts: `Math.random` 20, `Date.now` 0, `performance.now` 1, localStorage 2.
- Not read / not here: the Chakra Petch font loads from Google Fonts over the network (falls back to system-ui offline); why anything is as it is (INTENT UNKNOWN); how it feels.
