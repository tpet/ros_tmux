# ROS Launch Alternative using tmux (ros_tmux)

- An alternative to roslaunch using *tmux* terminal multiplexer.
- Each node is launched in a separate tmux window, under launch-specific session.
    - Session/window names: `<launch_name>:<node_name>`
- `Ctrl-C` forwards the signal to the nodes and stops the launcher. 
    - The windows remain open and are reused on restart.
    - Clients are not detached and can continue to monitor the windows.
- Logs are appended to `ros_tmux/log/<launch_name>/<node_name>.log`.

## Usage
```bash
ros_tmux <launch_path>
```

## Known Issues
- Syntax `ros_tmux <package> <launch_name>` not supported.
