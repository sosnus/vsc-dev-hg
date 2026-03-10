# vsc-dev-hg
Visual Studio Code Online Development Workspace for Hugo


# How to run it?
```bash
docker run -d \
  --name vsc-dev-hg \
  -p 40083:8080 \
  -v /var/docker-storage/vsc-dev-hg/workspace:/home/coder/workspace \
  -v vscode-data:/home/coder/.local \
  -e PASSWORD=changeme \
  --restart unless-stopped \
  sosnus/vsc-dev-hg
```


```bash
sudo mkdir /var/docker-storage/vsc-dev-hg/workspace
```

## If You have problem with access to storage
```bash
sudo chmod -R 777 /var/docker-storage/vsc-dev-hg/workspace
```

## stop container and remove storage
```bash
docker rm -f vsc-dev-hg && docker volume rm vscode-data
```


# Hugo

## Create new project
```bash

```



# Other

```bash
docker-compose build --no-cache

docker-compose up

```


another
```bash
docker compose down --volumes --remove-orphans && docker compose build --no-cache && docker compose up -d

docker compose build --no-cache && docker compose up -d

docker compose up -d --build --force-recreate

docker compose down --volumes --rmi all --remove-orphans && docker compose up -d --build
```

### Docker build&run without docker-compose
```bash
docker build -t vsc-dev-hg .
docker run -d \
  --name vsc-dev-hg \
  -p 8082:8080 \
  -v ./workspace:/home/coder/workspace \
  -v vscode-data:/home/coder/.local \
  -e PASSWORD=changeme \
  --restart unless-stopped \
  vsc-dev-hg
```

```bash
docker run -d \
  --name vsc-dev-hg \
  -p 8082:8080 \
  -v ./workspace:/home/coder/workspace \
  -v vscode-data:/home/coder/.local \
  -e PASSWORD=changeme \
  --restart unless-stopped \
  vsc-dev-hg
```


## Build

```bash
sudo docker buildx create --use --name multi-platform-builder
```