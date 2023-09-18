# README.md for Maze Solver

## Table of Contents
1. [Introduction](#introduction)
2. [Dependencies](#dependencies)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Classes](#classes)
    - [Node](#node)
    - [StackFrontier](#stackfrontier)
    - [QueueFrontier](#queuefrontier)
    - [Maze](#maze)
6. [Methods](#methods)
7. [Contributing](#contributing)
8. [License](#license)

## Introduction
This Python script is designed to solve a maze problem. It reads a maze from a text file and uses a stack-based frontier to find the path from the start point 'A' to the goal point 'B'.

## Dependencies
- Python 3.x
- PIL (Pillow) for image output

## Installation
1. Clone the repository.
2. Install the required packages.
    ```bash
    pip install Pillow
    ```

## Usage
1. Create a text file representing the maze. Use 'A' for the start, 'B' for the goal, and '#' for walls.
2. Run the script.
    ```bash
    python maze.py <maze_file.txt>
    ```
3. The script will output the solution in the terminal and generate an image.

## Classes

### Node
- Represents a state in the maze.
- Attributes: `state`, `parent`, `action`

### StackFrontier
- Implements a stack-based frontier.
- Methods: `add`, `contains_state`, `empty`, `remove`

### QueueFrontier
- Inherits from StackFrontier.
- Overrides the `remove` method to implement a queue.

### Maze
- Represents the maze.
- Attributes: `start`, `goal`, `walls`, `solution`
- Methods: `print`, `neighbors`, `solve`, `output_image`

## Methods

- `print()`: Prints the maze.
- `neighbors(state)`: Returns possible actions and states from a given state.
- `solve()`: Solves the maze.
- `output_image(filename, show_solution=True, show_explored=False)`: Outputs the maze and its solution as an image.
