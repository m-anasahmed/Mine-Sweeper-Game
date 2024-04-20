# Mine-Sweeper-Game

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

### Description

- **Working of Game :**
- The Minesweeper game begins by prompting the user to select a difficulty level: Beginner, Intermediate, or Advanced. Based on the chosen level, the board's side length and the number of mines are determined.
- Two 2D arrays, `realBoard` and `myBoard`, are initialized to represent the actual game board and the player's view, respectively. Initially, all cells on both boards are set to `-`, indicating they are empty.
- Mines are then randomly placed on the `realBoard` according to the selected difficulty level, and their positions are stored in the `mines` array. The main game loop (`playMinesweeper` function) continues until either a mine is opened or all non-mine cells are revealed (`movesLeft` becomes 0).
- During each iteration, the current state of `myBoard` is displayed using `printBoard`. The player selects a cell by entering its row and column coordinates. If it's the first move and the selected cell is a mine, the mine is relocated to ensure the player's first move is safe.
- For each empty cell selected, the number of adjacent mines is calculated and displayed on `myBoard` using `countAdjacentMines`. If a cell with a mine is opened, the game ends with a "You lost!" message, revealing all mine locations. Conversely, if all non-mine cells are opened, the game concludes with a "You won!" message.
- Additionally, the game offers a cheat mode (`cheatMinesweeper`) to view mine locations and a feature to replace a mine (`replaceMine`) to guarantee the player's first move safety.

---

#### Summary

- The game uses a 2D array to represent the board.
- Mines are randomly placed based on the selected difficulty.
- Players reveal cells to find non-mine areas.
- The game ends if a mine is revealed or all non-mine cells are opened.

