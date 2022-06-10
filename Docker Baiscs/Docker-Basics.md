## Installation
Follow guide: https://docs.docker.com/get-docker/

> Existing user needs to be added to Docker group after installation in Linux.

Command:
`sudo usermod -aG docker $USER`

### Testing if installation was successful
`docker run hello-world`

Error
> docker: Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?.

If you get this error try out the following command:
`systemctl start docker`
More info: https://stackoverflow.com/questions/44678725/cannot-connect-to-the-docker-daemon-at-unix-var-run-docker-sock-is-the-docker

## Experiment 1 - Working with Prebuilt images

**Scenario**
Let's say we have a website and we want to Dockerize it. How do we do it? A website is basically = The cotent (or code) + The server.

So we would need to create a container that can host and serve the images.

### Let's adventure
Docker has a wide range of prebuilt images. So it makes sense to go and explore the Docker Hub and try to find an appropiate image.

As we are want our container to be a web server, the first thing we are going to try is finding a [httpd](https://stackoverflow.com/questions/34681936/what-is-httpd-exactly) base image.

> When searching for images it is use official docker images or by verified publishers.

> We also should keep our images lean and not complicate it as we need to maintain and update the base image to protect against future security vulnerabilites.

Second type of server I wanted to experiment with was nginx image.

Pulling an image example:
`docker pull httpd`

Running the httpd image: `docker run --name httpd -p 8080:80 -d httpd:2.4`

Checking the status of the container: `docker ps`



