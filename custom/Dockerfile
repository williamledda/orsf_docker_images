FROM ros:noetic-robot-focal

RUN apt update && sudo apt install --no-install-recommends -y \
	nano \
	less \	
	net-tools \
	xterm \
	terminator \
	python-pip3 \
	ros-noetic-joy \
	ros-noetic-turtle* \
	ros-noetic-rqt-graph \
	&& rm -rf /var/lib/apt/lists/*

RUN useradd -ms /bin/bash rosdev && adduser rosdev sudo
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
RUN echo 'source "/opt/ros/$ROS_DISTRO/setup.bash"' >> /home/rosdev/.bashrc

USER rosdev
