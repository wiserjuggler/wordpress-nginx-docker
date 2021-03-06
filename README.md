# Wordpress docker deployment with nginx, mariadb and phpmyadmin.

## Prerequisites

1. Docker Engine
[Docker engine Installation Guide](https://docs.docker.com/engine/install/)
2. Docker Compose
[Docker compose Installation Guide](https://docs.docker.com/compose/install/)
3. git
[git installtion instruction](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
 
## 1. Clone Repository
```bash
 git clone https://github.com/wiserjuggler/wordpress-nginx-docker.git
 ```
## 2. Run Docker-Compose
Run the following command to start a container based on your image
```docker
cd wordpress-nginx-docker
```
```docker
docker-compose up -d
```
## 3. Configure Nginx

```bash
path=$(docker inspect nginx | grep -i  "/*_nginx/_data" | awk '{print substr($2,2, length($2)-3);}')
```
```bash
cp -f default.conf /$path
```
```bash
docker container restart nginx 
```

## Cleanup 
If you just want to clean up the data of a particular docker-compose stack, run

```bash
docker-compose down -v --rmi all --remove-orphans 
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[VD](https://github.com/varundhiman)
