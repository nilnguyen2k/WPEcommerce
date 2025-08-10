# WPEcommerce

A Dockerized setup for running a WordPress-based e-commerce platform with Portainer and Caddy.

## 1. Preparation

1. Create a **`.env`** file inside the `wpshop` folder and fill in all environment variables based on the **`example.env`** file.  
2. Open the **`Caddyfile`** and replace:
   - `{$SHOP_DOMAIN}` → with the actual domain for your WordPress site.  
   - `{$PORTAINER_DOMAIN}` → with the actual domain for Portainer.

## 2. Start Services

### Start Portainer
```bash
docker compose -f ./portainer-docker-compose.yml up -d
```
### Start Wordpress
```bash
docker compose -f ./wpshop/portainer-docker-compose.yaml up -d
```
### Start Caddy
```bash
docker compose -f ./caddy/portainer-docker-compose.yaml up -d
```
