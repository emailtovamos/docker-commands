# docker-commands
Commands for docker, Dockerfile and docker-compose

- Once Dockerfile is ready, the command to build the image: 

  ```docker build -t <imagename>:tag .```
  
- Build Docker image with no cache. This is very important if you are making changes to the same file and Docker may think it hasn't changed. So it is always safe to use the following command to build Docker image when in doubt: 

  ```docker build --no-cache -t <imagename>:tag .```
  
  e.g.

  ```docker build --no-cache -t emailtovamos/game-repo:v02 .```
  
- If you want to push the image to registry of docker: 

  ```docker push <imagename>:tag```

- Access a process running on docker (e.g. having the number: 1e91702267b7 ): 

  ```docker exec -it 1e91702267b7 sh```
  
- Get ip of docker machine: 

  ```docker-machine ip```
