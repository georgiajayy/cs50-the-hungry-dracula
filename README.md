# The Hungry Dracula

A retro Game Boy-inspired 2D arcade catching game built for Harvard's CS50 Week 0 in Scratch.

## Controls & Scoring

* **Move:** Left and Right arrow keys to steer Dracula across the arena.
* **Blood:** `+1` point
* **Silver Sword:** `+3` points
* **Garlic:** `-2` points
* **Time Limit:** 30-second round — score as high as possible before the timer runs out.

## How It Works

* **State & Broadcast Architecture:** The game moves from a custom Title Screen and Instructions screen into the Game Arena using `start game` broadcasts to synchronize player controls, falling items, audio, and the 30-second countdown loop, then fires a `game over` broadcast when time expires to display the **Restart** button and reset the round.
* **Parameterized Spawning (`reset drop (delay)`):** Falling item sprites use a custom block (`reset drop (delay)`) that takes a `delay` input, resets the sprite's position along the top of the arena, waits for the specified delay, and reveals the item during active play.
* **CS50 Week 0 Mechanics:** Built with custom pixel-art backdrops and sprites, `score` and `timer` variables, conditional collision/boundary checks, and `repeat until` loops.

## CS50 Week 0 Requirements

* **At least two sprites (not the default Scratch cat):** Implemented with five custom sprites (`dracula_sprite`, `Blood`, `Garlic`, `Silver Sword`, and `Restart Button`).
* **At least three scripts total:** Built across more than twelve scripts managing screen transitions, background audio, Dracula's movement, countdown timing, item drops, scoring, and game resets.
* **At least one condition:** Used `if < > then` logic to validate screen transitions, detect left/right key presses, check collisions with Dracula, and reset items when they fall past the bottom of the arena.
* **At least one loop:** Used `repeat until <(timer) = (0)>` loops to keep Dracula, falling items, the countdown clock, and audio synchronized during each 30-second round.
* **At least one variable:** Tracked active game state using `score` and `timer` variables to update points and end the round when time runs out.
* **At least one custom block (`My Blocks`):** Defined a reusable `reset drop (delay)` custom procedure with a `delay` parameter to control item respawning.

## Files in This Repository

* `The Hungry Dracula.sb3` — Full Scratch project archive containing all sprites, pixel-art backdrops, sound effects, and scripts.
