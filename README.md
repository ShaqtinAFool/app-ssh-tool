# Tip command
```bash
# Init VM
docker machine init
docker machine start

# Build on local
docker build -t app-ssh-tool .
docker build -t app-ssh-tool . --no-cache
docker build -t auoplatform.azurecr.io/app-ssh-tool . --no-cache
docker exec -it app-ssh-tool bash

# Push image to ACR
docker tag app-ssh-tool auoplatform.azurecr.io/app-ssh-tool:latest
docker images
docker push auoplatform.azurecr.io/app-ssh-tool:latest

# Run container
docker run --name app-ssh-tool -p 8080:80 localhost/app-ssh-tool

docker stop app-ssh-tool
docker rm app-ssh-tool
```
