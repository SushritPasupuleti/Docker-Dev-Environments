# Docker Dev Environments

Setting up Docker Containers to be used as Dev Environments, that allows for editing from the host with realtime updates.

## Getting Started

Spin up the containers with:

```bash
docker compose up -d
```

Edit files in the `server` directory, and they will be synced to the container.

Access the container with:

```bash
docker container ls
# Copy the container ID
docker exec -it <container_id> sh
```

## Use cases

- For languages with garbage package managers, like Python, which lead to hard to reproduce environments.

## General Tips

- You can optionally setup your entire Editor+LSP inside the container if you are running a different toolchain version.

- Make sure that you add dependency directories like `node_modules` to your `.dockerignore` file, so that you don't sync the entire `node_modules` directory to the container.
