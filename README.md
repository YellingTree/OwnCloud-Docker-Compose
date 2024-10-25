# OwnCloud-Docker-Compose
Fully Configured Owncloud Installation behind a Reverse Proxy with Onlyoffice enabled

### Letsencrypt Container
- Set your email for `DEFAULT_EMAIL`

### Owncloud Container
- Configure `VIRTUAL_HOST` and `LETSENCRYPT_HOST` to your domain for owncloud
- Configure `OWNCLOUD_DOMAIN` to your domain for owncloud
- Configure `OWNCLOUD_TRUSTED_DOMAINS` to your cloud domain and office domain (eg. cloud.domain.com,office.domain.com)
- Change `OWNCLOUD_ADMIN_USERNAME=ExampleAdmin` to a desired account name

### Onlyoffice Container
- Configure `VIRTUAL_HOST` and `LETSENCRYPT_HOST` to your domain for onlyoffice
 
### Before Starting
- Make sure you edit the env.example file and set your passwords. Then rename the file to .env
- Ensure you've downloaded or recreated `my_custom_proxy_settigns.conf` in the same directory as your docker-compose.yml file

### Startup
Run docker compose up -d to start your containers, navigate to your cloud domain, and configure the server with a MYSQL Database using settings shown in the compose file under the `owncloud` container
