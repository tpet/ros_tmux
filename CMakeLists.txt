cmake_minimum_required(VERSION 2.8.3)
project(ros_tmux)

install(
    PROGRAMS
        scripts/ros_tmux
        scripts/ros_tmux_run
        scripts/ros_tmux_node
    DESTINATION ${CMAKE_INSTALL_PREFIX}/bin
)

install(
    FILES
        config/ros_tmux.conf
    DESTINATION ${CMAKE_INSTALL_PREFIX}/share
)
