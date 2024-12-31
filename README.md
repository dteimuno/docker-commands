# Docker Commands Reference

This repository documents various Docker commands learned during Docker training. Below is a list of commands with explanations to help understand their purpose and usage.

## Commands Overview

### Basic Docker Commands
- **`docker`**
  - Displays general information and options for Docker.

### Running Containers
- **`docker container run --publish 80:80 nginx`**
  - Runs an Nginx container and maps port 80 on the host to port 80 in the container.
- **`docker container run --publish 80:80 --detach nginx`**
  - Runs an Nginx container in detached mode and maps port 80 on the host to port 80 in the container.

### Stopping Containers
- **`docker container stop <container_id>`**
  - Stops a running container, replacing `<container_id>` with the actual container ID (e.g., `cf51a6aaa488`).

### Listing Containers
- **`docker container ls -a`**
  - Lists all containers, including both running and stopped ones.

### Named Containers
- **`docker container run --publish 80:80 --detach --name webhost nginx`**
  - Runs an Nginx container in detached mode with the name `webhost` and maps port 80 on the host to port 80 in the container.
- **`docker container top webhost`**
  - Displays running processes in the `webhost` container.

### Getting Help
- **`docker container --help`**
  - Shows help for container-related Docker commands.

### Removing Containers
- **`docker container rm -f <container_id>`**
  - Forces the removal of a container, replacing `<container_id>` with the actual container ID (e.g., `29f586463313`).

### Running a MongoDB Container
- **`docker run --name mongo -d mongo`**
  - Runs a MongoDB container in detached mode with the name `mongo`.
- **`docker ps`**
  - Lists all running containers.
- **`docker top mongo`**
  - Displays running processes in the `mongo` container.

### Host System Commands
- **`ps`**
  - Displays information about active processes on the host system.
- **`ps aux`**
  - Displays detailed information about all processes on the host system.
- **`ps aux | grep <process_name>`**
  - Filters processes matching `<process_name>` (e.g., `mongo`).

### Starting Stopped Containers
- **`docker start mongo`**
  - Starts the `mongo` container if it was previously stopped.

### Verifying Status
- **`docker ps`**
  - Confirms that the `mongo` container is running.
- **`ps aux | grep mongo`**
  - Confirms the `mongo` process is active on the host system.

## Notes
- Replace placeholders like `<container_id>` and `<process_name>` with the actual values specific to your environment.
- Use `docker container ls` to quickly identify running containers and their IDs.

## License
This repository is licensed under the MIT License.
