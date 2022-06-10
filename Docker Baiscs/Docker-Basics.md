## Installation
Follow guide: https://docs.docker.com/get-docker/

## Docker Fundamentals

The Docker daemon (dockerd) listens for Docker API requests and manages Docker objects such as images, containers, networks and volumes. It can communicate with other daemons to manage Docker services.

It is a persistent background process that manages the containers on a single host -> Probably explains why running the docker desktop app costs so much battery power.

The Docker desktop app is basically the UI version of the docker daemon.

> Existing user needs to be added to Docker group after installation in Linux.

Command:
`sudo usermod -aG docker $USER`

