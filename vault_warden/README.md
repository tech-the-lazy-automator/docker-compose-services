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

### Deploy Vaultwarden on Docker
1. Create directories and files
```bash
# Create vaultwarden directory
mkdir vaultwarden

# Navigate to vaultwarden
cd vaultwarden

# Create docker-compose.yml file
touch docker-compose.yml
```
2. Copy the content of docker-compose.yml from repo to your file
3. Modify volume directory path
4. Deploy the container
```bash
# Deploy docker container
docker compose up -d
```
4. Vaultwarden web UI available at `http://<ip-address>:82`
5. Add reverse proxy for Vaultwarden in [Nginx Proxy Manager](../nginx_proxy_manager/README.md)
6. Create Vaultwarden account and login

### Disable Sign Ups
1. Once logged in, set `SIGNUPS_ALLOWED: "false"` in *docker-compose.yml*
2. Redeploy container
```bash
# Redeploy docker container
docker compose up -d
```

### Browser extension
**Google Chrome** - Click on three dot Menu ( ⋮ ) at top right > Extensions > Manage Extensions > Web Store
1. Search "Bitwarden Password Manager"
2. Select the one from bitwarden.com
3. Add to browser and open extension
4. Before logging in, switch server from *bitwarden.com* to *self-hosted*
5. Add server URL - `<your-vaultwarden-domain>` (Created using NPM)
6. Login using Email & Master Password

### Add Items
Name - Application name  
Username - Email / Username (Can be generated)  
Password - Application password (Recommended: Use generator)  
TOTP - You can add 2FA  
URI - Application URL (Multiple allowed)  

## Resources
- [Docker Image for Vaultwarden](https://hub.docker.com/r/vaultwarden/server)