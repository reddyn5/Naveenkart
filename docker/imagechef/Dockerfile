FROM ubuntu:16.04
MAINTAINER "naveeen"
RUN apt-get update
RUN apt-get install -y net-tools
RUN apt-get install -y vim
RUN apt-get install -y openssh-server
RUN useradd -m -d /home/naveen -s /bin/bash naveen
RUN echo "naveen:naveen" | chapasswd
RUN sed -i '21i reddy ALL=(ALL:ALL)'
USER reddy ALL /etc/sudoers
RUN apt-get install sudo
ENTRYPOINT service restart && bash
