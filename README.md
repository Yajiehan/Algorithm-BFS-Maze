# Maze Problem Solver

This repository contains a Python implementation of solving maze problems using the Breadth-First Search (BFS) algorithm.

## Problem Description

Given a maze where 0 represents open paths and 1 represents walls, along with a starting point (startX, startY) and a destination point (destinationX, destinationY), this algorithm determines if a ball can roll from the starting point to the destination, following the rules of rolling only in cardinal directions until hitting a wall.

## Algorithm Steps

1. Create a queue to store positions (x, y) and their respective paths.
2. Enqueue the starting point into the queue and mark it as visited.
3. Use a BFS loop to explore directions from the dequeued position.
4. If the destination is encountered during exploration, return True.
5. If the queue becomes empty without reaching the destination, return False.

## Usage

1. Clone this repository: `git clone https://github.com/your-username/maze-problem-solver.git`
2. Modify the `maze` grid, `start`, and `destination` variables in the provided Python script.
3. Run the script: `python maze_solver.py`

## Example

```python
from maze_solver import hasPath

# Example maze represented as a 2D grid (0: passage, 1: wall)
maze = [
    [0, 0, 1, 0, 0],
    [0, 0, 0, 0, 0],
    [0, 0, 0, 1, 0],
    [1, 1, 0, 1, 1],
    [0, 0, 0, 0, 0]
]

start = (0, 4)
destination = (4, 4)

print(hasPath(maze, start, destination))  # Output: True
