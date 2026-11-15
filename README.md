[![make.fun · best-game-01](https://make.fun/badge/best-game-01.svg)](https://make.fun/bounty/best-game-01?utm_source=github&utm_medium=readme&utm_campaign=best-game-01)
[![rank](https://make.fun/badge/best-game-01/aris189/best-game-01/rank.svg)](https://make.fun/bounty/best-game-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=best-game-01)
[![reward](https://make.fun/badge/best-game-01/aris189/best-game-01/reward.svg)](https://make.fun/bounty/best-game-01?utm_source=github&utm_medium=readme&utm_campaign=best-game-01)

# Neon Void — a neon space shooter

A complete browser game: pilot your ship through waves of invaders, break the
capital ships guarding waves 5 and 10, and chase the high score. No build step,
no network — plain static files under `game/`, playable in desktop Chrome.

## How to play

- **Move:** Arrow keys / WASD, or drag on touch
- **Shoot:** hold Space (or keep touching)
- **Pause:** P · **Mute:** M · **Start / restart:** Enter

Enemies come in three kinds — drifters, weavers, and shooters that fire back.
A capital ship guards wave 5 and wave 10; destroy the wave-10 capital ship to
win the campaign, then keep flying in endless mode. Power-ups drop from
wrecked enemies: **S** spread shot, **H** shield, **R** rapid fire, and a rare
extra life.

## Run it

Serve the folder and open it in a browser:

```sh
node serve.ts
```

Then open http://localhost:8080/.

The entry program `main.ts` (Node 22, standard library only) copies `game/`
and `screenshots/` to `/output` and writes `/output/dossier.json`:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

Screenshots in `screenshots/` are real renders of the game's own code:
`1-start.jpg` (title), `2-play.jpg` (mid-fight, wave 3), `3-end.jpg` (game
over). They are produced with `?shot=start|play|end&seed=1`, so the same
seed always renders the same frame.

---

Built for the make.fun bounty [best-game-01](https://make.fun/bounty/best-game-01)
