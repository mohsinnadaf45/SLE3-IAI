# Maze Path-Finding System — BFS & DFS

## Overview

This project is a Maze Path-Finding System developed in Python.

The system takes a grid maze containing walls, a start cell, and a goal cell. It finds a path using:
- BFS (Breadth-First Search)
- DFS (Depth-First Search) with a depth limit of 1000

The system compares both algorithms using path length, nodes expanded, and execution time.

## Objectives

- Find a path through a maze using BFS and DFS.
- Compare BFS and DFS performance.
- Measure execution time.
- Count expanded nodes.
- Understand the system architecture using the C4 Model.

## Algorithms

### BFS
BFS uses a queue and finds the shortest path when all moves have equal cost.

### DFS
DFS uses a stack and searches with a depth limit of 1000.

## C4 Architecture

### Level 1 — Context
The student provides a maze and selects BFS or DFS. The system returns the path, path length, nodes expanded, and execution time.

### Level 2 — Containers
1. Maze Input Module
2. Search Engine
3. Neighbour Generator
4. Visited Set / Memory
5. Experiment Runner
6. Output Module

### Level 3 — Components
The Search Engine contains:
- Frontier
- Node Expander
- Visited Set
- Goal Test
- Path Reconstructor
- Depth Limit Check

BFS uses a queue as its Frontier, while DFS uses a stack.

### Level 4 — Code
Important functions:
- `generate_maze(size)`
- `get_neighbors(maze, cell)`
- `bfs(maze, start, goal)`
- `dfs(maze, start, goal, limit=1000)`
- `reconstruct_path(parents, goal)`
- `run_experiments.py`

## Project Structure

```text
AI_Augmented_Workflow/
├── generate_maze.py
├── maze_solver.py
├── run_experiments.py
├── results.json
├── charts/
├── flame_graph/
└── README.md
```

## How It Works

```text
Input Maze
    ↓
Choose BFS / DFS
    ↓
Search Engine
    ↓
Generate Neighbours
    ↓
Check Visited Cells
    ↓
Find Goal
    ↓
Reconstruct Path
    ↓
Display Results
```

## Experiments

The project tests maze sizes such as:
- 20 × 20
- 40 × 40
- 70 × 70

The experiment runner executes the algorithms multiple times and measures execution time using `time.perf_counter()`.

## AI Contribution

AI tools used:
- Claude
- GitHub Copilot

AI was used for assistance with the C4 architecture layout, diagram generation, documentation wording, and earlier code assistance.

The student selected the maze system, decided the architecture, checked the components against the BFS/DFS code, and reviewed the final work.

## Author

**Mohasin Riyaj Nadaf**  
PRN: **25UAM130**  
Division: **B**  
Course: **02AML204 — Introduction to Artificial Intelligence**

## Conclusion

The project demonstrates maze path finding using BFS and DFS and represents the system using all four levels of the C4 model. BFS and DFS mainly differ in how they manage the Frontier: BFS uses a queue and DFS uses a stack.
