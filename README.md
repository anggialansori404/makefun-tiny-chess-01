# tiny-chess-01 — round 2

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/anggialansori404/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/anggialansori404/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,068 bytes of Python (`main.py` unpacks and runs an
lzma-packed engine): 0x88 board, negamax with PVS, LMR, null-move pruning,
quiescence with check evasions, transposition table, killers, MVV-LVA,
tapered piece-square evaluation, pawn-structure terms. Fixed 40,000-node
budget per move — no clock, fully deterministic.
