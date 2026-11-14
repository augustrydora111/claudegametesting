# Game Brief: Magnet Crew

> Read from the game by `/reverse-document` for `prototypes/magnet-crew/`, as it came in at tag
> `baseline/magnet-crew`. What the code cannot say is marked `INTENT UNKNOWN`.

## In your words
"I co-built a minigame prototype in another session"

**Pitch:** One shift, sixty seconds: press and hold scrap to swarm it with little magnet bots and drag the whole scrapyard into the furnace. *(inferred (strong))*

**Genre:** one-thumb swarm-management arcade, score attack *(guessed)*

**Controls:** press and hold a part to stream bots onto it; tap the furnace or the PULSE button to recall every bot. Touch or mouse (pointer events). *(inferred (strong))*

**Question:**

**Hooks:** the crew is both your currency and your tool: power cells grow the crew, scrap scores, and overcharging a part with extra bots makes it fly faster. *(guessed)*

**Intent:**

## Look and references
- Look: top-down industrial scrapyard on a dark steel floor with an 80 px grid, rivets and oil stains; small yellow tread bots with a red horseshoe magnet and a cyan eye; brass gears, steel hex nuts and engine blocks as scrap; glowing cyan power cells; a glowing furnace at the bottom with a hazard stripe and smoke. Palette: steel `#2b3038`, amber `#ffb627` (scrap, credits), cyan `#4fe3ff` (bots' magnetism, cells). Chakra Petch font. *(inferred (strong))*
- References: INTENT UNKNOWN
- View: 2D · Camera: fixed top-down, fills the screen, built for portrait phones.

## First minute
The start card explains the rules and CLOCK IN starts the shift with 6 bots parked above the furnace and 9 parts on the floor. A hint says "press & hold a part"; holding a small power cell lifts it at once and returns 2 new bots, which teaches the snowball: cells first, then the heavy scrap that is worth more. *(inferred (strong))*

## Challenge
No way to lose: the 60-second clock is the pressure. Parts need as many clamped bots as their weight, new parts spawn every 3.2 s and grow heavier as the crew grows (max weight ≈ 0.8 × bots, up to 25), and bots tied up on parts are not free. *(inferred (strong))*

## Core loop
- Hold a part to stream free bots onto it until its gauge fills.
- The part lifts and floats to the furnace: a cell becomes new bots, scrap becomes credits.
- A bigger crew lifts heavier, more valuable scrap; repeat until the shift ends.

## Goal & fail state
- Score as many credits as possible in a 60-second shift; the best score is saved. The shift always ends on the timer, with credits, bots, parts smelted and peak working bots shown.

## Features
- [x] 60-second shift with timer, crew and credits HUD
- [x] Press-and-hold streams bots onto a part; weight gauge; lift and float to furnace
- [x] Power cells build bots; scrap pays credits scaled by weight
- [x] Overcharge: extra bots (up to 2× weight) speed a part up
- [x] Pulse recall (button or tap the furnace)
- [x] Part spawning that scales with crew size
- [x] Start card, end card with stats, best score saved locally
- [x] Haptics, sparks, floating text, furnace smoke

## Keep
-

## Avoid
-

## Out of scope
-

## Build order
1. The game as it came in (all `[x]` above).

---
**Kill condition:**

**Who it's for / what they feel:** INTENT UNKNOWN

**Games you love / don't:** INTENT UNKNOWN
