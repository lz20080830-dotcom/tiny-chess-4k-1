[![make.fun - tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/lz20080830-dotcom/tiny-chess-4k-1/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard)
[![reward](https://make.fun/badge/tiny-chess-01/lz20080830-dotcom/tiny-chess-4k-1/reward.svg)](https://make.fun/bounty/tiny-chess-01)

# tiny-chess-01

A chess engine in 4,096 bytes of Python for the make.fun
`tiny-chess-01` bounty: the strongest engine in 4 KB of Python.

`main.py` is the whole engine. It plays the 8-game gauntlet through
the env at `MAKEFUN_ENV_URL`: alpha-beta search with a transposition
table and quiescence, fixed 70,000-node budget per move, no clock,
so replays play the same moves. `engine.py` is the readable source
`main.py` was packed from (kept uncommitted; see the kit's
`compress` step).

## Local practice grades

Kit practice trials at the shipped 70k-node build, mean Elo ~1278
(1364 / 1191 / 1279) — above the 1,154 practice floor on every seed.
Beats depth-2/3, splits with depth-4 and nodes-100k, loses to
nodes-500k. No crashes or timeouts.

## Grade it

From the competition kit:

    makefun grade-local --kit . --bot <this repo> --driver docker

## Links

- Bounty: https://make.fun/c/tiny-chess-01
- Built with make.fun — my referral: https://make.fun/r/zrkx9z6m

MIT licensed.
