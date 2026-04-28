# Unity Kinect Maze

## Overview
This repository contains the source code and Unity project files for the Kinect Maze application. The project utilizes C# scripting to handle dynamic entity movement, rotation mechanics, and game state management within a 3D environment. 

[cite_start]This repository serves as the central integration hub for collaborative development, enforcing strict version control protocols to maintain build stability[cite: 76].

## Core Mechanics & Scripts
The gameplay logic is driven by modular C# components located in the `Assets/Scripts/` directory:
* `MoveForward.cs` - Handles the primary forward translation logic for entities.
* `EnemyMover.cs` - Governs the pathing and movement behavior for hostile elements.
* `Rotator.cs` & `Turning.cs` - Manages local and global rotation transformations.
* `RestartButtonController.cs` - Controls the UI event listeners for resetting the game state.

## Repository Architecture & Branching Strategy
[cite_start]To prevent merge conflicts and ensure a stable deployment pipeline, this project strictly adheres to a multi-branch workflow[cite: 111, 112]:
* **`main`**: The protected production branch. [cite_start]Only stable, fully reviewed code is merged here[cite: 113, 125]. [cite_start]Direct commits are prohibited[cite: 197].
* **`development`**: The primary integration branch. [cite_start]All feature branches merge here via Pull Requests for testing and peer review[cite: 112, 128].
* [cite_start]**`feature/*`**: Isolated branches for developing individual mechanics (e.g., `feature/enemy-movement`, `feature/ui-update`)[cite: 112, 131].

## Version Control Rules
* **Cache Avoidance:** Unity auto-generates gigabytes of cache data. The `Library/`, `Temp/`, `Builds/`, and `Logs/` directories are strictly ignored via the `.gitignore` file to prevent repository bloat[cite: 109, 155].
* [cite_start]**Continuous Integration:** Always pull the latest changes from the `development` branch before beginning a new session to ensure local code is up to date[cite: 198].
* [cite_start]**Commit Standards:** Use clear, descriptive commit messages (e.g., `feat: added enemy speed modifier`, `fix: resolved rotator collision bug`)[cite: 198].
