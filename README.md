# docker-commands
Commands for docker, Dockerfile and docker-compose

- Once Dockerfile is ready, the command to build the image: 

  ```docker build -t <imagename>:tag .```
  
- If you want to push the image to registry of docker: 

  ```docker push <imagename>:tag```

- Access a process running on docker (e.g. having the number: 1e91702267b7 ): 

  ```docker exec -it 1e91702267b7 sh```
  
- Get ip of docker machine: 

  ```docker-machine ip```
