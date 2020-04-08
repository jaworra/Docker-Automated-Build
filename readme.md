# Automated Docker builds
- CI/CD pipeline, build new docker from GitHub into DockHub. 


#### Containers and Virtualisation 
Runs on Docker for reproducibility and CI/CD approach, there is a Dockerfile and and premade image on referenced Docker Hub.


- Manual build/run

```
docker build -t [image_name] .
docker run -p 8888:8888 [image_name] .
```

- Docker Compose

```docker-compose up```  mounts the directory and starts the container.
```docker-compose down```  destroys the container

- For maintained image
https://hub.docker.com/repository/docker/jaworra/docker-automated-builds
- Cheatsheet commands
```
docker container ls #show all containers
docker rmi $(docker images -f "dangling=true" -q) #stop dangling processes
docker stop $(docker ps -a -q) #stop all containers
docker system prune -a`  #clean all
docker -f jupyter.dockerfile -t jupyter:latest .  #build specific docker file
docker login --username=[username] --pasword-stdin[password]
docker commit [containerid] [username/imagename:tag]
docker push [dockerimage]
``` 
