
## Docker workflow

1. Setup nginx:latest image
2. Create custom docker image
3. Create a new container
4. Start, Stop and etc container


## Docker useful commands
```bash
# Setup Nginx
$ docker pull nginx:latest

# Create custom docker image
$ docker build -t hidocker-nginx:v0.0.1 .

# Verify Nginx image
$ docker images

# Create a new container
$ docker create --name hidocker -p 3000:3030 hidocker-nginx:v0.0.1

# Remove one or more containers
$ docker rm hidocker

# Start container
$ docker start hidocker

# Stop container
$ docker stop hidocker

# Run a command in hidocker container
$ docker exec -ti hidocker /bin/bash

# Save one or more images to a tar archive
$ docker save -o hidocker-nginx.v0.0.1.tar hidocker-nginx:v0.0.1

# Load an image from a tar archive
$ docker load -i ./hidocker-nginx.v0.0.1.tar
```
