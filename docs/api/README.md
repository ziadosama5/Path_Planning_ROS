# API Reference

This section documents public, user-facing APIs exposed by this repository. With the current contents, the primary public interface is a ROS launch file that spawns a TurtleBot3 in Gazebo.

- [ROS Launch: `turtlebot3_maze.launch`](./ros_launch/turtlebot3_maze.md)

When algorithmic nodes and libraries are added (e.g., BFS/DFS planners), document them here:

- Nodes: parameters, topics, services, actions
- Libraries: public classes/functions with signatures and examples
- Messages: custom message/service definitions

## Documentation template

Use the following template when adding new public APIs.

### Module or Node: name

- Description: What it does
- Parameters: name — type — description — default
- Topics:
  - Publishes: `/topic` — message — description
  - Subscribes: `/topic` — message — description
- Services/Actions: name — type — description
- Errors: common failure modes

Example:
```bash
rosrun your_package your_node _param:=value
```

