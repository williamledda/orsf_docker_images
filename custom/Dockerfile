FROM ros:noetic-robot-focal

RUN apt update && sudo apt install --no-install-recommends -y \
	less \	
	net-tools \
	xterm \
	ros-noetic-joy \
	ros-noetic-turtle* \
	&& rm -rf /var/lib/apt/lists/*

RUN useradd -ms /bin/bash rosdev && adduser rosdev sudo
RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers

USER rosdev

ENTRYPOINT ["/ros_entrypoint.sh"]
CMD ["bash"]