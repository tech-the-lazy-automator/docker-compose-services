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

### Deploy Nginx Proxy Manager on Docker
1. Create directories and files
```bash
# Create nginx_proxy_manager directory
mkdir nginx_proxy_manager

# Navigate to nginx_proxy_manager
cd nginx_proxy_manager

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
5. Nginx Proxy Manager web UI available at `http://<ip-address>:81`
6. Login using [default credentials](#important-notes)

### Generate SSL certificate

#### DuckDNS
1. Create domain
2. Set current IP - Server's local IP > Click on update IP
3. Copy token (Required in NPM for SSL)

#### Nginx Proxy Manager
1. SSL Certificates > Add SSL Certificate
2. Add domains - *Add domains to request SSL*
    1. `<domain>.duckdns.org` - Domain
    2. `*.<domain>.duckdns.org` - All sub-domains
3. Enable "I Agree to the Let's Encyrpt Terms of Service"
4. Enable "Use a DNS Challenge"
    1. DNS Provider - DuckDNS
    2. Credentials File Content - *Replace `<your-duckdns-token>` with your token*
        ```txt
        dns_duckdns_token=<your-duckdns-token>
        ```
    3. (Optional) If getting error - Set **Propagation Seconds** to 30
5. Save changes

### Setup Reverse Proxies

1. Hosts > Proxy Hosts > Add Proxy Host > Details
2. Domain Names - `<sub-domain>.<domain>.duckdns.org`
3. Scheme - *(http/https) where service is accessible*
4. Forward Hostname/IP - *`<ip-address>` of service*
5. Forward Port: *`<port>` where service is exposed*
6. For additional security, enable below options:
    - Cache Assets
    - Block Common Exploits
    - Websockets Support
7. Switch to SSL tab
8. Select SSL Certificate
9. Enable below options:
    - Force SSL
    - HTTP/2 Support
10. Save changes

## Important Notes
Default credentials of Nginx-Proxy-Manager:
- Email: admin@example.com
- Password: Changeme

## Resources
- [DuckDNS Official Website](https://www.duckdns.org/)
- [Docker Image for Nginx-Proxy-Manager](https://hub.docker.com/r/jc21/nginx-proxy-manager)
