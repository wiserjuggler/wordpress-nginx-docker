# Wordpress docker deployment with nginx, mariadb and phpmyadmin.

## Prerequisites

1. Docker Engine
[Docker engine Installation Guide](https://docs.docker.com/engine/install/)
2. Docker Compose
[Docker compose Installation Guide](https://docs.docker.com/compose/install/)
3. git 

## Git installation 
  Centos 
 ```bash
 sudo yum install git
 ```
  Debian
 ```bash
 sudo apt install git
 ```
  windows
  ```powershell
 @"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command " [System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
  
choco install git
 ```
 
## 1. Clone from git repository
```bash
 git clone https://github.com/wiserjuggler/wordpress-nginx-docker.git
 ```
## 2. Run Docker-Compose
Run the following command to start a container based on your new image
```docker
cd wordpress-nginx-docker
docker-compose up -d
```
## 3. Configure Nginx
Run the following command to build your bulletin board image
```bash
sudo cp wordpress.conf /var/lib/docker/volumes/wordpressnginxdocker_nginx/_data/default.conf          
```
## 4. Restart Nginx 
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
