# Docker Commands Cheatsheet

My handy cheatsheet for Docker commands.

## Containers

- `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`
  - Run a new container from an image.
- `docker ps [OPTIONS]`
  - List running containers.
- `docker ps -a [OPTIONS]`
  - List all containers (including stopped ones).
- `docker start [OPTIONS] CONTAINER`
  - Start a stopped container.
- `docker stop [OPTIONS] CONTAINER`
  - Stop a running container.
- `docker restart [OPTIONS] CONTAINER`
  - Restart a container.
- `docker pause CONTAINER`
  - Pause a running container.
- `docker unpause CONTAINER`
  - Unpause a paused container.
- `docker rm [OPTIONS] CONTAINER`
  - Remove one or more containers.
- `docker logs [OPTIONS] CONTAINER`
  - Fetch the logs of a container.
- `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`
  - Run a command in a running container.
- `docker top [OPTIONS] CONTAINER [ps OPTIONS]`
  - Display the running processes of a container.
- `docker stats [OPTIONS] [CONTAINER...]`
  - Display a live stream of container resource usage statistics.
- `docker inspect [OPTIONS] OBJECT`
  - Display detailed information about an object (container, image, etc.).

## Images

- `docker images [OPTIONS] [REPOSITORY[:TAG]]`
  - List Docker images.
- `docker pull [OPTIONS] NAME[:TAG|@DIGEST]`
  - Pull an image or a repository from a registry.
- `docker build [OPTIONS] PATH | URL | -`
  - Build an image from a Dockerfile.
- `docker rmi [OPTIONS] IMAGE [IMAGE...]`
  - Remove one or more images.
- `docker image prune [OPTIONS]`
  - Remove unused images.
- `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`
  - Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE.

## Volumes

- `docker volume ls [OPTIONS]`
  - List Docker volumes.
- `docker volume create [OPTIONS] [VOLUME]`
  - Create a new volume.
- `docker volume inspect [OPTIONS] VOLUME`
  - Display detailed information about a volume.
- `docker volume rm [OPTIONS] VOLUME [VOLUME...]`
  - Remove one or more volumes.

## Networks

- `docker network ls [OPTIONS]`
  - List Docker networks.
- `docker network create [OPTIONS] NETWORK`
  - Create a new network.
- `docker network inspect [OPTIONS] NETWORK [NETWORK...]`
  - Display detailed information about a network.
- `docker network rm [OPTIONS] NETWORK [NETWORK...]`
  - Remove one or more networks.

## Compose

- `docker-compose up [OPTIONS] [SERVICE...]`
  - Start and attach to containers for a service.
- `docker-compose down [OPTIONS]`
  - Stop and remove containers, networks, and volumes defined in a `docker-compose.yml` file.
- `docker-compose build [OPTIONS] [SERVICE...]`
  - Build or rebuild services defined in a `docker-compose.yml` file.
- `docker-compose ps [OPTIONS] [SERVICE...]`
  - List containers for a service in a `docker-compose.yml` file.
- `docker-compose logs [OPTIONS] [SERVICE...]`
  - View output from containers started by a `docker-compose.yml` file.
- `docker-compose exec [OPTIONS] SERVICE COMMAND [ARGS...]`
  - Run a command in a running service container.
- `docker-compose pull [SERVICE...]`
  - Pull images for services defined in a `docker-compose.yml` file.
- `docker-compose restart [OPTIONS] [SERVICE...]`
  - Restart services.
- `docker-compose down -v`
  - Remove containers, networks, volumes, and images defined in a `docker-compose.yml` file.

## Registry

- `docker login [OPTIONS] [SERVER]`
  - Log in to a Docker registry.
- `docker logout [SERVER]`
  - Log out from a Docker registry.
- `docker search [OPTIONS] TERM`
  - Search the Docker Hub for images.
- `docker push [OPTIONS] NAME[:TAG]`
  - Push an image or a repository to a registry.
- `docker pull [OPTIONS] NAME[:TAG|@DIGEST]`
  - Pull an image or a repository from a registry.

## System

- `docker version [OPTIONS]`
  - Show the Docker version information.
- `docker info [OPTIONS]`
  - Display system-wide information.
- `docker system df [OPTIONS]`
  - Show Docker disk usage.
- `docker system prune [OPTIONS]`
  - Remove all unused data (containers, volumes, networks, images).
- `docker events [OPTIONS]`
  - Get real-time events from the server.
- `docker inspect [OPTIONS] OBJECT`
  - Display detailed information about an object (container, image, etc.).
- `docker logs [OPTIONS] CONTAINER`
  - Fetch the logs of a container.
- `docker cp [OPTIONS] CONTAINER:SRC_PATH DEST_PATH|-`
  - Copy files/folders from a container to the host.
- `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`
  - Run a command in a running container.
- `docker diff [OPTIONS] CONTAINER`
  - Inspect changes to files or directories on a container's filesystem.
- `docker events [OPTIONS]`
  - Get real-time events from the server.
- `docker import [OPTIONS] file|URL|- [REPOSITORY[:TAG]]`
  - Import the contents from a tarball to create a filesystem image.

## Miscellaneous

- `docker --help`
  - Show help for Docker commands.
- `docker image history IMAGE`
  - Show the history of an image.
- `docker system events [OPTIONS]`
  - Get real-time events from the server.
- `docker system prune [OPTIONS]`
  - Remove all unused data (containers, volumes, networks, images).
