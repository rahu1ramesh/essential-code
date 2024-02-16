| Command | Explanation | Use Case |
|---|---|---|
| **`docker build`** | Builds an image from a Dockerfile. | Building a custom Docker image for a web server. |
| **`docker pull`** | Pulls an image or a repository from a registry. | Pulling the latest version of a database image from Docker Hub. |
| **`docker push`** | Pushes an image or a repository to a registry. | Pushing a customized Docker image to a private registry. |
| **`docker run`** | Runs a command in a new container. | Running a containerized application for testing. |
| **`docker run --name <container_name>`** | Sets a custom name for the container. | `docker run --name my_container nginx` Runs an Nginx container with the custom name "my_container". |
| **`docker run -d <image:tag>`** | Runs the container in detached mode, meaning it runs in the background. | `docker run -d nginx` Starts an Nginx container in detached mode, allowing you to continue using the terminal. |
| **`docker run -p <host_port>:<container_port> <image:tag>`** | Maps a port from the host to the container. | `docker run -p 8080:80 nginx` Runs a container on port 80 inside the container, mapped to port 8080 on the host. |
| **`docker start`** | Starts one or more stopped containers. | Starting a previously stopped container. |
| **`docker stop`** | Stops one or more running containers. | Gracefully stopping a running container. |
| **`docker restart`** | Restarts one or more containers. | Restarting a container after configuration changes. |
| **`docker exec`** | Runs a command in a running container. | Executing a shell command inside a running container. |
| **`docker exec -it bash`** | Runs a command in a running container interactive shell. | Accessing an interactive shell in a running container. |
| **`docker ps`** | Lists running containers. | Checking the status of running containers. |
| **`docker ps -a`** | Lists all containers, both running and stopped. | Viewing the history of containers on the system. |
| **`docker images`** | Lists all images on the local system. | Displaying a list of Docker images available locally. |
| **`docker rmi`** | Removes one or more images. | Deleting an unused Docker image. |
| **`docker rm`** | Removes one or more containers. | Cleaning up stopped containers. |
| **`docker pull [registry:]image[:tag]`** | Pulls an image or a repository from a registry. | Pulling an image from a private registry. |
| **`docker network`** | Manages Docker networks. | Creating and configuring Docker networks. |
| **`docker volume`** | Manages Docker volumes. | Managing data volumes for Docker containers. |
| **`docker logs <container_name>`** | Fetches logs of a container. | Inspecting container logs for troubleshooting. |
| **`docker inspect <container_name / image_id / short_id>`** | Returns low-level information about a container, image, or task. | Retrieving detailed information about Docker resources. |
| **`docker-compose`** | Manages multi-container Docker applications. | Orchestrating the deployment of multiple Docker containers. |
