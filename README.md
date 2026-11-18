# makefun-tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/anggialansori404/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/anggialansori404/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

**A full chess engine in 4,089 bytes.** `main.py` (Python 3, standard
library only) plays through the make.fun env protocol and searches with
a negamax alpha-beta: iterative deepening under a fixed 40,000-node
budget (no clock, so replays are move-for-move identical), PVS,
quiescence over captures/promotions with check evasions, a
transposition table, null-move pruning, late-move reductions, check
extensions, and MVV-LVA + killer + history move ordering.

The board is 0x88 with incremental Zobrist keys and an incremental
evaluation: material plus tapered piece-square tables (king table
blended by game phase) and a bishop-pair bonus. Repetition, the
50-move rule and the 200-ply material adjudication are honoured in
search. The source is minified and lzma-packed behind a small
self-extracting stub; the readable engine was verified with perft
(startpos d4 = 197,281; Kiwipete d3 = 97,862) and a fuzz oracle before
packing, and the packed file itself was replay-verified.

Local practice trials against the house gauntlet (6 games each):
trial 0 — Elo 1364 (3W 1D 2L); trial 1 — Elo 1654 (5W 0D 1L), with
wins against every rung up to nodes-500k (1,596 anchor).
