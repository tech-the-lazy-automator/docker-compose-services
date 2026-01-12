# #13 - Nginx Proxy Manager
[![Thumbnail](https://img.youtube.com/vi/acturgE4TmE/maxresdefault.jpg)](https://www.youtube.com/watch?v=acturgE4TmE)

## File Structure
```bash
nginx_proxy_manager
├── volumes
│   ├── data
│   └── letsencrypt
└── docker-compose.yml
```

## Instructions

#### Deploy Nginx Proxy Manager on Docker
1. Create directories and files.
```bash
# Create nginx_proxy_manager directory
mkdir nginx_proxy_manager

# Navigate to nginx_proxy_manager
cd nginx_proxy_manager

# Create docker-compose.yml file
touch docker-compose.yml
```
2. Copy the content of docker-compose.yml from repo to your file.
3. Deploy the container.
```bash
# Deploy docker container
docker compose up -d
```
4. Nginx Proxy Manager web UI available at `http://<ip-address>:81`
5. Login using [default credentials](#important-notes).

## Important Notes
Default credentials of Nginx-Proxy-Manager:
- Email: admin@example.com
- Password: Changeme

## Resources
- [DuckDNS Official Website](https://www.duckdns.org/)
- [Docker Image for Nginx-Proxy-Manager](https://hub.docker.com/r/jc21/nginx-proxy-manager)
