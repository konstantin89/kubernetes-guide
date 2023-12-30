# hello-world kubernetes example

## Installing tools
[Install kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/)  
[Install docker](https://www.simplilearn.com/tutorials/docker-tutorial/raspberry-pi-docker)  

## Running the application

### Starting Docker container registry on local machine
``` bash
docker pull registry:2
docker run -d -p 5000:5000 --name local-registry registry:2
```
### Building server docker container
``` bash
# Build container 
docker build -t localhost:5000/my-server:latest .

# Push container to registry
docker push localhost:5000/my-server:latest
```
