# Mine-Sweeper-Game

Absolutely! Here's a presentation-style explanation of the Minesweeper game code:

---

### Minesweeper Game in C++

#### Introduction

- **Objective**: Create a Minesweeper game in C++.
- **Tools Used**: Standard C++ libraries for input-output, mathematical calculations, string operations, and time-related functions.

---

#### Game Setup

- **Macros and Global Variables**
  - `BEGINNER`, `INTERMEDIATE`, `ADVANCED`: Difficulty levels
  - `MAXSIDE`: Maximum board side length
  - `MAXMINES`: Maximum number of mines

- **Global Variables**
  - `SIDE`: Current board side length
  - `MINES`: Current number of mines

---

#### Utility Functions

1. **isValid(row, col)**
   - Checks if a cell `(row, col)` is within the board.

2. **isMine(row, col, board)**
   - Checks if a cell contains a mine.

3. **makeMove(x, y)**
   - Gets user's move input.

4. **printBoard(myBoard)**
   - Prints the current game board.

5. **countAdjacentMines(row, col, mines, realBoard)**
   - Counts adjacent mines for a given cell.

---

#### Game Logic

1. **playMinesweeperUtil(myBoard, realBoard, mines, row, col, movesLeft)**
   - Recursive function to play the game.

2. **placeMines(mines, realBoard)**
   - Places mines randomly on the board.

3. **initialise(realBoard, myBoard)**
   - Initializes the game board.

4. **cheatMinesweeper(realBoard)**
   - Reveals mine locations (cheat mode).

5. **replaceMine(row, col, board)**
   - Replaces a mine with an empty space.

---

#### Main Game Function

- **playMinesweeper()**
  - Main game loop.
  - Displays the current board.
  - Handles user moves and game outcomes.

---

#### Game Initialization and Difficulty Selection

- **chooseDifficultyLevel()**
  - Allows the user to select the game difficulty.

- **main()**
  - Entry point of the program.
  - Calls `chooseDifficultyLevel` and `playMinesweeper`.

---

#### Summary

- The game uses a 2D array to represent the board.
- Mines are randomly placed based on the selected difficulty.
- Players reveal cells to find non-mine areas.
- The game ends if a mine is revealed or all non-mine cells are opened.

---
