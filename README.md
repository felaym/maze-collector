# Maze Collector

A simple maze game built with C# and Windows Forms.

Collect all the prizes, avoid the walls, and reach the finish to complete the game.

## Features

- Grid-based maze
- Player movement with keyboard controls
- Collectible prizes
- Walls and obstacles
- Finish point unlocked after collecting all prizes
- Game timer
- Score tracking
- Game results saved to a text file
- Simple graphical interface with custom textures

## Controls

| Key | Action |
| --- | --- |
| `W` / `↑` | Move up |
| `S` / `↓` | Move down |
| `A` / `←` | Move left |
| `D` / `→` | Move right |
| `Esc` | Exit the game |

## How to Play

1. Start the game.
2. Move the player around the maze.
3. Collect all available prizes.
4. Once all prizes are collected, the finish becomes available.
5. Reach the finish to complete the game.
6. Your score and completion time are saved to `game_results.txt`.

## Technologies

- C#
- .NET
- Windows Forms
- GDI+ (`System.Drawing`)

## Project Structure

The game is built around a few main components:

- `GameObject` — base class for objects placed on the game field.
- `Player` — controls the player's position and appearance.
- `Wall` — blocks player movement.
- `Prize` — collectible game objects.
- `Finish` — completes the game after all prizes are collected.
- `GameField` — manages the game grid, objects, movement, score, and timer.
- `MainForm` — handles the Windows Forms UI and rendering.

## Object System

Game objects use a common `GameObject` base class with:

- Custom textures
- Drawing order (`ZIndex`)
- Walkability rules
- Player interaction logic

This allows different objects to define their own behavior without putting all game logic into `GameField`.

## Running the Game

1. Clone the repository.
2. Open the project in Visual Studio.
3. Restore the NuGet/.NET dependencies if required.
4. Build the project.
5. Run the application.

The game expects its textures in the `Resources` directory:

```text
Resources/
├── player.png
├── wall.png
├── star.png
└── finish.png
