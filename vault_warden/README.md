# #14 - Vaultwarden
[![Thumbnail](https://img.youtube.com/vi/kJOkmxKGKEg/maxresdefault.jpg)](https://www.youtube.com/watch?v=kJOkmxKGKEg)

## File Structure
```bash
vaultwarden
├── volumes
│   └── data
└── docker-compose.yml
```

## Instructions

#### Deploy Vaultwarden on Docker
1. Create directories and files.
```bash
# Create vaultwarden directory
mkdir vaultwarden

# Navigate to vaultwarden
cd vaultwarden

# Create docker-compose.yml file
touch docker-compose.yml
```
2. Copy the content of docker-compose.yml from repo to your file.
3. Deploy the container.
```bash
# Deploy docker container
docker compose up -d
```
4. Vaultwarden web UI available at `http://<ip-address>:82`
5. Add reverse proxy for Vaultwarden in Nginx Proxy Manager.
6. Create Vaultwarden account and login.

## Resources
- [Docker Image for Vaultwarden](https://hub.docker.com/r/vaultwarden/server)