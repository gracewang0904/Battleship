# Battleship
Battleship is a two-player strategy game where you take turns guessing coordinates to find and sink all of your opponent’s hidden ships before they sink yours. This program is a Battleship game simulator supporting multi-turn gameplay with real-time hit/miss feedback. **Codebase is private. Please reach out if you'd like access**.

## 🧠 Project Overview

This Battleship game has the following components:
- A 10x10 2D grid
- A user-controlled car
- Two rectangular obstacles
- A tracking window tracking the movement of the car

Example grid layout:

```..-.......  // Row 0 occupies board[0] to board[9] \n
..*.......  // Row 1 occupies board[10] to board[19]
-.BDDD.-..  // ...
..B.......
..*.......  // We would say that the * on this row is at R4 C2 (row 4, column 2)
..-....S..
.....--*..
.......S..
..........
.........-  // Row 9 occupies board[90] to board[99]
```

What it can do:
- Ship placements
- Board printing
- Real-time hit/miss/sink feedback

## 🔧 Technologies & Tools

C, Bash script

## 🎯 How to Play Battleship

- The game is played on a 10×10 board with several ships placed either vertically or horizontally.  
- Players take turns firing shots at specific board locations using **row and column coordinates**.
- Each shot reveals whether it was a:
  - **Hit**: the target square is part of a ship — displayed as `*`  
  - **Miss**: the square does not contain a ship — displayed as `-`
- You’ll receive printed feedback after each shot:
  - `"Hit at R<row> C<col>"`  
  - `"Miss at R<row> C<col>"`

### 💥 Sinking Ships
- Each ship has a certain length. Once all of its segments are hit, it's considered **sunk**.
- You'll see a message like:  
  `"Destroyer was sunk!"`

### 🛠️ Usage Example

Translated Input:
```bash
# Shots fired at:
# (0,2), (1,2), (2,2), (3,2), (4,2), (5,2), (2,4), (9,9), (6,7), (2,3), (2,5)
```

Sample Output:
```
Miss at R0 C2
Hit at R1 C2
Hit at R2 C2
Hit at R3 C2
Hit at R4 C2
Battleship was sunk!
Miss at R5 C2
Hit at R2 C4
Miss at R9 C9
Hit at R6 C7
Hit at R2 C3
Hit at R2 C5
Destroyer was sunk!
```
