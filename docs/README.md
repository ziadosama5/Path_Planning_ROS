# Project Documentation

Welcome to the documentation for `Path_Planning_ROS`.

This repository contains materials for a ROS-based TurtleBot3 navigation demo in a 10x10 maze-like world using BFS and DFS concepts. At present, only a launch file and assets are checked in; source nodes for BFS/DFS are not included in the repository. This docs site provides a structure to capture APIs, usage, and examples as the codebase evolves.

- See [API Reference](./api/README.md)
- See [Usage Guide](./usage/README.md)
- See [Examples](./examples/README.md)

## Contents

- Overview of the ROS launch configuration used to spawn a TurtleBot3 in Gazebo
- Guidance for environment setup and running the simulation
- Templates for documenting public APIs, nodes, topics, and components when code is added

## Project overview

- Robot: TurtleBot3 (`burger`, `waffle`, or `waffle_pi`)
- Simulator: Gazebo, via `gazebo_ros`
- Launch file: `Path planning/Req2/launch/turtlebot3_maze.launch`
- Planning concepts: BFS and DFS on a grid map (algorithmic nodes not present in this repo)
