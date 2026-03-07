# vsc-dev-hg
Visual Studio Code Online Development Workspace for Hugo

```
docker-compose build --no-cache

docker-compose up

```


another
```
docker compose down --volumes --remove-orphans && docker compose build --no-cache && docker compose up -d

docker compose build --no-cache && docker compose up -d

docker compose up -d --build --force-recreate

docker compose down --volumes --rmi all --remove-orphans && docker compose up -d --build
```
