# Metadata Docker Setup


## Prerequisites

Ensure you have the following installed on your system:
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Check Docker Installed
```sh
docker version
```

### 1. Log in to Docker
Before pulling images, authenticate with docker credentials:
```sh
docker login
```

### 2. Download the Docker Compose File
Use `curl` or `wget` to download the `docker-compose.yml` file:
```sh
curl -O https://raw.githubusercontent.com/Karthikeyanl2000/metadata/main/docker-compose.yml
# or
wget https://raw.githubusercontent.com/Karthikeyanl2000/metadata/main/docker-compose.yml
```

### 3. Build and Start the Containers
Run the following command to build and start all services in detached mode:
```sh
docker compose -f docker-compose.yml up --build -d
```
The `--build` flag ensures that any changes to the Dockerfile are applied before starting the containers.

### 4. View Running Containers
```sh
docker ps
```

### 5. Stop the Containers
To stop the running containers, use:
```sh
docker compose -f docker-compose.yml down
```

