# private cloud - docker - ssl proxy - wordpress

The title says it all:
that's what you will find in my github repositories.

## moe lab

This repository provides
various Docker containers that are based on docker-compose.
Applications provided are as follows:

- Wordpress - Content Management System
- Nextcloud - Private Cloud
- Traefik - Proxy with SSL Encryption (via Let's Encrypt)
- Portainer - Container Management
- Ouroboros - Automatic Image Updates

You can find the repository under
<https://github.com/moeb98/moe-lab>.

All the applications are proxied via traefik 2.0 which takes care
of SSL encryption. Thus, all frontend applications are connected
to a frontend network called traefik_proxy while backend systems
are only connected to the backend network.

Since we are using Docker containers, this relies on external
networks that need to be created before using the docker-compose
files:

```bash
docker network create traefik_proxy
docker network create backend
```

Each of the containers can now be fired up using

```bash
docker-compose up -d
```

## fotografie child theme

fotografie is a great wordpress theme for a photography portfolio.
The child theme
adds some features for featured content and wordpress pages while
improving the responsive design for different (mobile) devices.

You can find the repository under
<https://github.com/moeb98/fotografie-child>.

## smart home

My smart home is based on node-red and includes Philips Hue,
Shelly, Osram Lightify, Logitech Harmony, Zigbee including a
Zigbee USB stick on Raspberry Pi. Repo is still private, stay
tuned...
