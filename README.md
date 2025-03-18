# Metadata Docker Setup


## Prerequisites

Ensure you have the following installed on your system:
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

### 1. Log in to Docker
Before pulling images, authenticate with Docker using your credentials:
```sh
docker login
```

### 2. Download the Docker Compose File
Use `curl` or `wget` to download the `docker-compose.yml` file:
```sh
curl -O <compose-file-url>
# or
wget <compose-file-url>
```

### 3. Build and Start the Containers
Run the following command to build and start all services in detached mode:
```sh
docker-compose up --build -d
```
The `--build` flag ensures that any changes to the Dockerfile are applied before starting the containers.

### 4. View Running Containers
```sh
docker ps
```

### 5. Stop the Containers
To stop the running containers, use:
```sh
docker-compose down
```

## Configuration
Modify the `docker-compose.yml` file to customize the services as needed. Environment variables can be configured using a `.env` file.

## Logs
To view logs for a specific container, use:
```sh
docker-compose logs -f <service-name>
```

