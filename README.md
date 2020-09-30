# docker-commands
Commands for docker, Dockerfile and docker-compose

- Get current Docker version

  ```docker -version```

- Once Dockerfile is ready, the command to build the image: 

  ```docker build -t <imagename>:tag .```
  
- Build Docker image with no cache. This is very important if you are making changes to the same file and Docker may think it hasn't changed. So it is always safe to use the following command to build Docker image when in doubt: 

  ```docker build --no-cache -t <imagename>:tag .```
  
  e.g.

  ```docker build --no-cache -t emailtovamos/game-repo:v02 .```
  
- Retag a local image with a new image name and tag before pushing to dockerhub:

  ```docker tag mylocalimage:1.0 myrepo/myimage:2.0```
  
- Pull a particular Docker image

  ```docker pull <imageName>```  

- If you want to push the image to registry of docker: 

  ```docker push <imageName>:tag```
  
- See all images: 

  ```docker images```

- Access a process running on docker (e.g. having the number: 1e91702267b7 ): 

  ```docker exec -it 1e91702267b7 sh```
  
- Get ip of docker machine: 

  ```docker-machine ip```
  
- Stop/Kill a container:

  ```docker stop <containerId>```
  ```docker kill <containerId>```
  
- Stop & Remove all containers: 

  ```docker stop $(docker ps -a -q)```
  ```docker rm $(docker ps -a -q)```

- docker-compose start

  ```docker-compose up```  

- docker-compose stop everything

  ```docker-compose down```  
  
- ssh into a running container

  ```docker exec -it <containerId> bash```

- login to your docker-hub

  ```docker login```
  
- logout of docker-hub

  ```docker logout```
  
- Delete image from local storge: 

  ```docker rmi <imageName>```

- List networks:

  ```docker network ls```
  
- Run a container from the Alpine version 3.9 image, name the running container “web” and expose port 5000 externally, mapped to port 80 inside the container:

  ```docker container run --name web -p 5000:80 alpine:3.9```
  
- Print the last 100 lines of a container’s logs:

  ```docker container logs --tail 100 web```  
  
- Stop a running container through SIGTERM:

  ```docker container stop web```
  
- Stop a running container through SIGKILL:

  ```docker container kill web``` 
