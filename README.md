# ITI - Docker Lab 🐋

## Task 1: Working with Docker Hello-world Image
### Objective
Learn how to run a container using the hello-world image and manage containers and images.

### Steps
#### 1. Run a Container with hello-world Image
```bash
 docker container run hello-world
```
#### 2. Check Container Status and Explain
```bash
  docker ps -a
The status of the hello-world container will likely be "Exited". The reason for this is that the hello-world container is designed to simply print a message and then exit
```
#### 3. Start the Stopped Container
```bash
docker start hello-world
```
#### 4. Remove the Container
```bash
```docker rm hello-world
#### 5. Remove the Image
```bash
```docker rmi hello-world or id container
---

## Task 2: Running Container with Ubuntu Image
### Objective
Run an Ubuntu container in interactive mode, create a file inside it, and manage containers.

### Steps
#### 1. Run Ubuntu Container in Interactive Mode
```bash
 docker container run -d --name u1 ubuntu
```
#### 2. Create a File inside the Container
```bash
 docker exec -it -u1 bash 
 touch hello-docker 
```
#### 3. Stop and Remove the Container
```bash
docker stop u1
docker rm u1 or container id 

```
#### 4. Check File Status
```bash
You can't directly check the file status after the container has been stopped and removed 
```
#### 5. What happened to hello-docker file?
```bash
```it will be lost 
#### 6. Remove All Stopped Containers
```bash
docker container prune

```
#### 7. Bonus: Remove All Containers in One Command
```bash
```docker container prune -f


---
## Task 3: Creating a Custom Nginx Docker Image
### Objective

vi Dockerfile in docker file write 
from nginx:alphine 

2- vi index.html
will write hello shimaa 

3-after created index.html i will open Dockerfile again to copy index.html
COPY index.html /usr/share/nginx/html/index.html

4-docker build -t custom-nginx .

5-docker run -d -p 8080:80 --name shimaa custom-nginx

6-docker ps 

7-curl localhost:8080






