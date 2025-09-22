# Usage Guide

This project uses ROS 1 and Gazebo with TurtleBot3. The provided launch file spawns a TurtleBot3 into a maze world.

## Prerequisites

- ROS 1 (Melodic/Noetic)
- Gazebo (9/11, matching your ROS distro)
- TurtleBot3 packages: `turtlebot3_description`, `turtlebot3_gazebo`
- `gazebo_ros`, `xacro`

On Ubuntu with ROS Noetic:
```bash
sudo apt update
sudo apt install ros-noetic-gazebo-ros ros-noetic-turtlebot3-description ros-noetic-turtlebot3-gazebo ros-noetic-xacro
```

## Environment

Set the TurtleBot3 model (if not already set):
```bash
export TURTLEBOT3_MODEL=burger
```

## Running the launch

Option A: Launch by file path (no package required):
```bash
roslaunch "/workspace/Path planning/Req2/launch/turtlebot3_maze.launch"
```

Option B: Use within a catkin package:
- Place the launch file under `your_package/launch/turtlebot3_maze.launch`
- Update any `$(find ...)` paths if package names differ
- Run:
```bash
roslaunch your_package turtlebot3_maze.launch
```

## Notes on world path

The launch file references a world via:
```
<arg name="world_name" value="$(find milestone2)/world/maze.world"/>
```
If the `milestone2` package is not present, replace with an absolute path to your world file or adjust to your package name.

## Next steps

When planner nodes (BFS/DFS) are added, include their parameters and topics under API docs and extend this usage guide with how to start planners and visualize paths.