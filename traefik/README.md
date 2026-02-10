# 45 - Traefik
[![Thumbnail](https://img.youtube.com/vi/7jwUh9_R_x8/maxresdefault.jpg)](https://www.youtube.com/watch?v=7jwUh9_R_x8)

## File Structure
```bash
docker/
└── docker_compose/
    └── traefik/
        ├── config/
        │   └── traefik.yml
        └── docker-compose.yml
```

## Instructions
### Deploy Traefik on Docker
1. Create directories and files
```bash
# Create traefik directory
mkdir -p traefik/docker_compose/traefik

# Navigate to traefik
cd traefik/docker_compose/traefik

# Create docker-compose.yml file
touch docker-compose.yml
```
2. Copy the content of docker-compose.yml from repo to your file
3. Modify volume directory path
4. Configure traefik.yml
```bash
# Create config directory
mkdir config

# Navigate to config
cd config

# Create traefik.yml file
touch traefik.yml
```
5. Copy the content of traefik.yml from repo to your file
6. Deploy the container
```bash
# Navigate to Docker Compose File Location
cd ..

# Deploy docker container
docker compose up -d

# View logs
docker logs traefik
```
7. Access Traefik Dashboard at `http://<ip-address>:8080`

## Resources
- [Docker Image for Traefik](https://hub.docker.com/_/traefik)