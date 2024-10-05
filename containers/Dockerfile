FROM osrf/ros:humble-desktop
ENV ROS_DISTRO=humble

# Ensure bash is used as the default shell
SHELL ["/bin/bash", "-c"]

# Add ROS setup to bashrc
RUN echo "source /opt/ros/${ROS_DISTRO}/setup.bash" >> /root/.bashrc

# Install X11 utilities for GUI applications
RUN apt-get update && apt-get install -y \
    x11-apps \
    xauth \
    x11-xserver-utils \
    && rm -rf /var/lib/apt/lists/*
