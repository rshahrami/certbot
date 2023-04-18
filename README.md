# certbot
## how to create certbot

change server name in nginx config and set your domain in file. comment certbot service befor running the flowing command

```
docker compose -f cert.yaml up -d
```
uncomment certbot service and run the flowing conmand

```
docker compose -f cert.yaml run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d example.org
```

set your domain instead of example.org
