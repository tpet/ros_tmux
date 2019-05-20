# ROS Launch Alternative using tmux (ros_tmux)

- An alternative to roslaunch using *tmux* terminal multiplexer.
- Each node is launched in a separate tmux window, under launch-specific session.
    - Session/window names: `<launch_name>:<node_name>`
- `Ctrl-C` forwards the signal to the nodes and stops the launcher. 
    - The launcher does not wait for the nodes to finish.
    - The windows remain open and are reused on restart.
- All logs are appended to `ros_tmux/log/<launch_name>/<node_name>.log`.

## Usage
```bash
ros_tmux_launch <launch_path>
TODO: ros_tmux_launch <package> <launch_name>
```

## Known Issues
- The launcher does not return if all nodes die (it can still be terminated manually).
- The launcher does not wait for nodes to finish on `Ctrl-C`.
