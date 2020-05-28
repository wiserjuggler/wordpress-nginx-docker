# wordpress-nginx-docker

## Prerequisites

1. A running server
2. Install Docker Engine
[Docker engine Installation Guide](https://docs.docker.com/engine/install/)
3. Install Docker Compose
[Docker compose Installation Guide](https://docs.docker.com/compose/install/)


## Setup Directories

Once you have Docker, Docker Compose installed, you can proceed to setup directories for the WordPress installation.

```bash
sudo mkdir wordpress-docker
cd wordpress-docker
sudo mkdir nginx wordpress
sudo mkdir -p logs/nginx
```

## Configure Nginx
Run the following command to build your bulletin board image
```bash
cd nginx
wget 
```

## Run your image as a container
Run the following command to start a container based on your new image
```docker
docker run --publish 8000:8080 --detach --name bb bulletinboard:1.0
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[VD](https://github.com/varundhiman)
