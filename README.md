# 2048-game-mips

## Introduction
This project is completed for COMP2611 Computer Organization. 2048 was originally written in JavaScript and CSS. Now it is re-implemented with MIPS assembly.

## Task Description
|  Procedure | Input   | Results | Description |
| ------------ | ------------ | ------------ | ------------ |
| `clear_map` | | all elements in `puzzle_map` will be set to 0. | clear up the 4x4 game grid. |
| `generate_a_random_tile` | | a new tile will randomly appear in an empty spot on the `puzzle_map` with a value drawn randomly from 2,4 equally. | refer to Section 2.2 |
| `slide` | $a0, $a1, $a2, $a3: the addresses of 4 elements in a column or row in the 4x4 game grid | the 4 numbers will be moved and merged in the direction of $a1 → $a3, according to the 2048 game rules. | refer to Section 2.1 |
| `check_win` | | $v0=1 if win, $v0=0 otherwise. | The game is won when a tile in `puzzle_map` has a value not less than the target game score (i.e., `input_target`). |
| `check_lose` | | $v0=1 if lose, $v0=0 otherwise | The game is lost if the `puzzle_map` is full and there are no more neighboring tiles that are combinable |
