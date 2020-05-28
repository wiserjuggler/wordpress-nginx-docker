# Wordpress-Nginx-Docker

## Prerequisites

1. A running server
2. Install Docker Engine
[Docker engine Installation Guide](https://docs.docker.com/engine/install/)
3. Install Docker Compose
[Docker compose Installation Guide](https://docs.docker.com/compose/install/)
4. Install git 
  
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
 git clone https://github.com/varundhiman/wordpress-nginx-docker.git
 ```
## 2. Setup Directories

Once you have Docker, Docker Compose installed, you can proceed to setup directories for the WordPress installation.

```bash
sudo mkdir wordpress-docker
cd wordpress-docker
sudo mkdir nginx wordpress logs
```

## 3. Configure Nginx
Run the following command to build your bulletin board image
```bash
sudo cp ~/wordpress-nginx-docker/wordpress.conf nginx/
```

## 4. Run Docker-Compose
Run the following command to start a container based on your new image
```docker
sudo cp ~/wordpress-nginx-docker/docker-compose.yml .
docker-compose up -d
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[VD](https://github.com/varundhiman)
