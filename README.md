# Build Your Own World

Java dungeon-crawler with deterministic, seed-based procedural world generation.

## Problem

Build a large, well-structured project from scratch: a tile-based game where the player explores a procedurally generated world, fights enemies in quiz battles, and collects health kits to survive. Every world has to be reproducible from a seed, including after a save and reload. Built as a course project for a Data Structures course at UC Berkeley.

## Approach

- **World generation:** places non-overlapping rooms from a seed and connects them with L-shaped hallways along a minimum spanning tree built with Kruskal's algorithm, so every room is reachable with minimal total hallway length.
- **Pathfinding:** BFS drives both avatar click-to-move (drawing and animating the shortest path) and enemy chasing.
- **Spawning:** a single precomputed BFS distance map gives O(1) spawn-distance checks, so enemies and items spread evenly across the map.
- **Combat:** a full-screen quiz-battle system with overlay rendering that preserves the world state underneath.
- **Save and load:** stores the seed and move history, then replays them to rebuild the exact world.
- Berkeley-themed pixel-art avatars on the StdDraw tile engine.

## Result

The same seed and inputs always rebuild the same world, including through save and load. The project emphasized large-project architecture, object-oriented design, and deterministic, testable generation.

## Tools

Java, StdDraw.

## Code availability

This project was completed as coursework. Per course policy, solution code isn't posted publicly here. I'm glad to walk through the implementation directly, reach out at vdkarthikeya@berkeley.edu.
