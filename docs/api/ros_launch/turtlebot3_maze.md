# ROS Launch: `turtlebot3_maze.launch`

Path: `Path planning/Req2/launch/turtlebot3_maze.launch`

This launch file spawns a TurtleBot3 model into a Gazebo world and publishes the robot description to the ROS parameter server.

## Arguments

- `model` (string, default: `$(env TURTLEBOT3_MODEL)`)
  - TurtleBot3 model to spawn. One of `burger`, `waffle`, `waffle_pi`.
- `x_pos` (number, default: `1`)
  - Spawn position X in meters.
- `y_pos` (number, default: `1`)
  - Spawn position Y in meters.
- `z_pos` (number, default: `0.0`)
  - Spawn position Z in meters.

## Includes

- `gazebo_ros/launch/empty_world.launch`
  - Args forwarded:
    - `world_name`: `$(find milestone2)/world/maze.world` (adjust to your package/path)
    - `paused`: `false`
    - `use_sim_time`: `true`
    - `gui`: `true`
    - `headless`: `false`
    - `debug`: `false`

## Parameters

- `robot_description` (string)
  - Loaded from `xacro`:
    - Command: `$(find xacro)/xacro --inorder $(find turtlebot3_description)/urdf/turtlebot3_$(arg model).urdf.xacro`

## Nodes

- Package: `gazebo_ros`
  - Type: `spawn_model`
  - Name: `spawn_urdf`
  - Args: `-urdf -model turtlebot3_$(arg model) -x $(arg x_pos) -y $(arg y_pos) -z $(arg z_pos) -param robot_description`

## Usage

Launch by absolute path:
```bash
export TURTLEBOT3_MODEL=burger
roslaunch "/workspace/Path planning/Req2/launch/turtlebot3_maze.launch" x_pos:=1 y_pos:=1
```

Launch within a catkin package:
```bash
roslaunch your_package turtlebot3_maze.launch model:=waffle
```

## Notes

- Ensure TurtleBot3 description and Gazebo packages are installed for your ROS distro.
- Replace `$(find milestone2)/world/maze.world` with a valid world path if the package `milestone2` is not available.