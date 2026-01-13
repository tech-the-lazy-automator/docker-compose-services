# #24 - Portainer
[![Thumbnail](https://img.youtube.com/vi/iYnXiyk8oZQ/maxresdefault.jpg)](https://www.youtube.com/watch?v=iYnXiyk8oZQ)

## File Structure
```bash
portainer
├── volumes
│   └── data
└── docker-compose.yml
```

## Instructions

#### Deploy Portainer on Docker
1. Create directories and files
```bash
# Create portainer directory
mkdir portainer

# Navigate to portainer
cd portainer

# Create docker-compose.yml file
touch docker-compose.yml
```
2. Copy the content of docker-compose.yml from repo to your file
3. Deploy the container
```bash
# Deploy docker container
docker compose up -d
```
4. Portainer web UI available at `http://<ip-address>:9000`
5. Create admin account and login

## Resources
- [Docker Image for Portainer Community Edition](https://hub.docker.com/r/portainer/portainer-ce)