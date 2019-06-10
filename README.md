# ROS Launch Alternative using tmux (ros_tmux)

- An alternative to roslaunch using *roslaunch* API and *tmux* terminal multiplexer.
- Each node is launched in a separate tmux window named `<node>` (from `__name:=<node>` argument), under session `ros_tmux` or `ros_tmux_<run_id>` (see Usage).
- `Ctrl-C` forwards the signal to the nodes and stops the launcher.
    - The windows remain open and are reused on restart.
    - Clients are not detached and can continue to monitor a specific node window.
- Node output is printed on screen and appended to the default log (from `__log:=<log>` argument), typically `~/.ros/log/<run_id>/<node>*.log`.

## Usage
```
ros_tmux <launch_path>
ros_tmux <package> <launch_name>
```
For tmux session specific to `run_id` use
```
ros_tmux_session=run_id ros_tmux [...]
```
