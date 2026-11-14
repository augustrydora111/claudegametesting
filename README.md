# Magnet Crew

A 60-second, one-thumb mobile game: run a crew of magnet bots in a scrapyard.
Press and hold a part to stream bots onto it; once enough clamp on, it lifts and
floats to the furnace. Power cells build more bots, scrap earns credits, and
Pulse calls every bot home.

## Play

Open [`prototypes/magnet-crew/index.html`](prototypes/magnet-crew/index.html) in
a browser. It is one self-contained file with no build step.

## Workflow

This project uses [Claude Code Game Studios](https://github.com/donchitos/claude-code-game-studios)
(framework v1.3.0): agents, skills and conventions live in `.claude/`, project
settings in `project.yaml`, and the layout is described in
`.claude/docs/directory-structure.md`. Start a Claude Code session at the repo
root and run `/start` or `/next-step`.

The game came in through `/prototype --from` and its original bytes are tagged
`baseline/magnet-crew`.
