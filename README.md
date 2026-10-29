# Abyss Run

A 3D deep-sea extraction game that runs in the browser. Dive a new trench every day, grab glowing salvage, and surface before your oxygen runs out. Die down there and the cargo is lost.

**Play:** https://benwintle73.github.io/abyss-run/

## How it plays

- Five depth zones, from the Sunlit Shallows to the Hadal Trench, each adding a new threat.
- Upgrade oxygen, hull, thrusters, floodlamp and sonar between dives.
- Every UTC day brings a new trench (same map for every player), a daily condition, a daily relic, a streak bonus and a fresh leaderboard.

Controls: WASD or arrow keys (or drag on touch screens), Space or the SONAR button to ping, P to pause.

## Tech

- Single `index.html`: Three.js 0.147 with bloom post-processing, Web Audio synth sound, no build step.
- Progress (credits, upgrades, streak) is saved in the player's browser.
- Daily leaderboard: Supabase (`rep-invaders` project), table `abyss_scores`, written only through the `abyss_submit` and read through the `abyss_board` RPCs. The publishable key in the page is safe to expose; the table itself has no public access.
