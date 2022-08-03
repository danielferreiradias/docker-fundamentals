# Docker - Essential Commands
- The below are the list of essential commands we are in need 

|     Commands                 |    Description                                  |
| ------------------------------- | --------------------------------------------- |
| docker ps | List all running containers |
| docker ps -a | List all containers stopped, running |
| docker stop container-id | Stop the container which is running |
| docker start container-id | Start the container which is stopped |
| docker restart container-id | Restart the container which is running |
| docker port container-id | List port mappings of a specific container |
| docker rm container-id or name | Remove the stopped container |
| docker rm -f container-id or name| Remove the running container forcefully |
| docker rmi image-id | Remove the docker image |
| docker images | Show docker images |
| docker tag nielbit/mynginx_image1:v1  nielbit/mynginx_image1:v1-release | Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE |
| docker push image-info | Push the image from docker hub repository |
| docker pull image-info | Pull the image from docker hub repository |
| docker pull stacksimplify/springboot-helloworld-rest-api:2.0.0-RELEASE | Pull the image from docker hub repository |
| docker run -d -e DBHOST="empdb" -e DBPORT="3306" -e DBUSER="root" -e DBPWD="abcd1234" -e DATABASE="awsecs" --name addemp --net awsecs -p 80:80 addemp:latest | Run a container with very options |
| docker exec -it container-name /bin/sh | Connect to linux container and execute commands in container |
| docker logout | Logout from docker hub |
| docker login -u username -p password | Login to docker hub |
| docker stats | Display a live stream of container(s) resource usage statistics |
| docker top container-id or name | Display the running processes of a container |
| docker version | Show the Docker version information |
| docker update --restart unless-stopped $(docker ps -q) | And this command will ensure all currently running containers will be restarted unless stopped |

