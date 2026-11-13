# 2048 Game

## Introduction

A browser version of the classic 2048 puzzle. Slide the tiles on a 4×4 board, merge equal numbers and try to reach the **2048** tile. The project separates the game logic (a `Game` class) from the interface (DOM manipulation), and was built to practice JavaScript classes, ES modules, event handling and SCSS.

## Live Preview

[View the deployed version](https://uuunemployed.github.io/js_game_2048/)

## Key Features

- **Classic 2048 rules:** tiles slide in the chosen direction, equal neighbours merge and add to the score.
- **Keyboard controls:** play with the arrow keys.
- **Touch controls:** swipe left, right, up or down on mobile devices (swipe threshold of 30px).
- **Score counter:** the current score updates after every move.
- **Start / Restart button:** starts a new game or resets the board to its initial state.
- **Game status messages:** hints before the start, a message when you win (2048 tile reached) and when you lose (no moves left).
- **Random new tiles:** after every valid move a new tile appears: `2` (90% chance) or `4` (10% chance). A move that changes nothing does not spawn a tile.

## How to Play

1. Press **Start**.
2. Use the arrow keys (or swipe on a touch screen) to move all tiles.
3. When two tiles with the same number touch, they merge into one.
4. Reach the **2048** tile to win. If the board is full and no merges are possible, the game is lost.
5. Press **Restart** to reset the game.

## Technical Requirements

To run this project, you will need:

- NPM (version 8.x or newer)

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/uuunemployed/js_game_2048.git
   ```

2. Navigate to the project directory:

   ```bash
   cd js_game_2048
   ```

3. Install dependencies:

   ```bash
   npm install
   # or
   yarn install
   ```

4. Run the project locally:

   ```bash
   npm start
   # or
   yarn start
   ```

After starting, the project is available at `http://localhost:8080` (the default Parcel port).

## Technologies Used

- **HTML5:** page structure, the game board is built with a table.
- **SCSS:** styling and tile colours for each value (2 to 2048).
- **JavaScript (ES6):** classes, modules, DOM API, keyboard and touch events.
- **Parcel:** bundler used to build and optimize the project.
- **ESLint, Stylelint, linthtml:** code style checks on every commit.
- **Git and GitHub:** version control, repository hosting and deployment (GitHub Pages).

## Challenges

- **Merge logic:** correctly sliding and merging tiles in all four directions, so that each tile merges only once per move.
- **Detecting a valid move:** comparing the board before and after a move so that a new tile spawns only when something changed.
- **Game status:** determining win and lose states (a full board with no equal neighbours means a loss).
- **Touch support:** recognising swipe direction by comparing horizontal and vertical distance.
