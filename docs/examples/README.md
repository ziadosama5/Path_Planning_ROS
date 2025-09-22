# Examples

Practical, runnable examples. Adapt paths as needed for your environment.

## Example: Spawn TurtleBot3 in Gazebo
```bash
export TURTLEBOT3_MODEL=burger
roslaunch "/workspace/Path planning/Req2/launch/turtlebot3_maze.launch"
```

## Example: Use a different starting pose
Edit args at runtime:
```bash
roslaunch "/workspace/Path planning/Req2/launch/turtlebot3_maze.launch" x_pos:=2 y_pos:=2 z_pos:=0.0
```

## Example: Package-based launch
```bash
roslaunch your_package turtlebot3_maze.launch x_pos:=1 y_pos:=1 model:=waffle
```