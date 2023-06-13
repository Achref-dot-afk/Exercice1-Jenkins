FROM jenkins/jenkins:lts

USER root

RUN curl -sSL https://get.docker.com/ | sh

USER jenkins

#This script is often used to install Docker on Linux-based systems. It retrieves the Docker installation script and passes it to the shell for execution, which installs Docker on the Docker image.
