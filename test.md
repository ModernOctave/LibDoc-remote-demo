---
title: Docker GUI
description:
---

# Setup
Use the following flags while making the container
```bash
-e DISPLAY=$DISPLAY -e QT_X11_NO_MITSHM=1 -v /tmp/.X11-unix:/tmp/.X11-unix
```

Before running a container give access to the XServer
```bash
xhost +local:root
```

# Toubleshooting
In case you get errors related to GPU try adding the following flag
```bash
--privileged
```

If want to use a NVIDIA GPU you should add the following flag
```bash
-e NVIDIA_DRIVER_CAPABILITIES=all
```

# Source
[ROS Wiki](http://wiki.ros.org/docker/Tutorials/GUI)