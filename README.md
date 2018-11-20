# Nginx-proxy
Config files to set up an nginx based reverse proxy which serves multiple websites and adds letsencrypt certificates. 

Based on

[jwilder/nginx-proxy](https://github.com/jwilder/nginx-proxy)

and

[JrCs/docker-letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion)

# Setup
Create a file called `.env` in the same folder as docker-compose.yml based on the following template
```
DEFAULT_HOST=<your default host>
SERVER_IP=<ip address>
```

To start run `./start`

Before starting containers with environment variables `VIRTUAL_HOST`/`LETSENCRYPT_X` make sure they are in the same docker network as the reverse-proxy container.
