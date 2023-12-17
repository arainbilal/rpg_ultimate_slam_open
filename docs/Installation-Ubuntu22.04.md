# Installation of Ultimate SLAM on Ubuntu 22.04

## Docker script

```
xhost +local:docker
docker run -it  \
    --privileged \
    --network=host \
    -v /dev/bus/usb:/dev/bus/usb \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -v /home/bilal/src/catkin_ws:/ws \
    -e DISPLAY=unix$DISPLAY \
    --name="noetic-container" \
    osrf/ros:noetic-desktop-full
```

# Build

## Catkin Tools
```
sudo apt-get install wget git libtool m4 automake
sudo apt-get install python3-catkin-tools
sudo apt install python3-vcstool
```

## Dependencies

```
cd src/
vcs-import < rpg_ultimate_slam_open/dependencies.yaml
```