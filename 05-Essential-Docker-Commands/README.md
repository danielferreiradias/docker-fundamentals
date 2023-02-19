# Docker - Essential Commands
- Below is the list of essential commands we need



|     Commands                 |    Description                                  |
| ------------------------------- | --------------------------------------------- |
| docker info | Info about docker architecture |
| docker ps | List all running containers |
| docker ps -a | List all containers stopped, running |
| docker container stop [ID/NAME] | Stop the container which is running |
| docker container start [ID/NAME] | Sart the container which is stop |
| docker container pause [ID/NAME] | Pause the container which is running |
| docker unpause [ID/NAME] | Unpause the container which is not running, but active |
| docker container start [ID/NAME] | Start the container which is stopped |
| docker container restart [ID/NAME] | Restart the container which is running |
| docker logs -f [ID/NAME] | Show container logs continually |
| docker container logs -n 5 [ID/NAME] | Show last five lines of container logs |
| docker container inspect [ID/NAME or IMAGE] | Inspect a container or image on JSON format |
| docker container prune | Remove all stopped containers |
| docker container ls -a | List all of your containers |
| docker image prune -a | Remove all images without at least one container associated to them |
| docker port [ID/NAME] | List port mappings of a specific container |
| docker container run --name MYCONTAINER --rm hello-world | Run "hello-world" container and remove it after execution |
| docker container rm [ID/NAME] | Remove the stopped container |
| docker container rm -f [ID/NAME] | Remove the running container forcefully |
| docker container stop $(docker ps -a -q) `&&` docker rm $(docker ps -a -q) | Stop and Remove all containers |
| docker rmi [IMAGE_ID] | Remove the docker image |
| docker images | Show docker images |
| docker search --filter "is-official=true" [IMAGE] | Search a specific official image in docker Hub repository |
| docker build -t myrepo/myimage Dockerfile | Build a image |
| docker tag nielbit/mynginx_image1:v1  nielbit/mynginx_image1:v1-release | Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE |
| docker push [IMAGE_INFO] | Push the image from docker hub repository |
| docker pull [IMAGE_INFO] | Pull the image from docker hub repository |
| docker pull stacksimplify/springboot-helloworld-rest-api:2.0.0-RELEASE | Pull the image from docker hub repository |
| docker run -d -e DBHOST="empdb" -e DBPORT="3306" -e DBUSER="root" -e DBPWD="abcd1234" -e DATABASE="awsecs" --name addemp --net awsecs -p 80:80 addemp:latest | Run a container with many parameters |
| docker container run -d -p 27017:27017 -e MONGO_INITDB_ROOT_USERNAME=mongouser -e MONGO_INITDB_ROOT_PASSWORD=mongopwd mongo | Run a container with many parameters |
| docker run --rm -it ubuntu:18.04 | Initialize a container with a interactive mode and finalize when exit it |
| docker container run --name ubuntu -itd ubuntu:18.04 | Initialize a container with a name 'ubuntu' with a interactive mode, enabling TTY and in a background mode |
| docker container exec -u root -it [ID/NAME] /bin/sh | Connect to linux container and execute commands with root in container |
| docker container exec -u root -d [ID/NAME] bash -c "echo 'any text' >> /tmp/lesson01" | Execute a container in background mode and append text in a archive |
| docker cp [ID/NAME]:/tmp/lesson01 . | Copy a archive from container to my current directory (. or $PWD) |
| docker cp lesson01 [ID/NAME]:/tmp/lesson01 | Copy a archive from PC to container |
| docker export [ID/NAME] \|gzip > export_container.tar.gz | Export a container with compression for persistence fins |
| zcat export_container.tar.gz \| docker import - export_new_container | Export a container as a image, after export use "docker container run -id export_new_container bash" |
| docker save export_new_container \|gzip -c > IMAGE.tar.gz | Export a container with compression for persistence fins |
| docker load < IMAGE.tar.gz | Import a container and after that, run it with "docker run -di export_new_container bash"
| docker login -u [USERNAME] -p [PASSWORD] | Login to docker hub |
| docker logout | Logout from docker hub |
| docker stats | Display a live stream of container(s) resource usage statistics |
| docker top [ID/NAME] | Display the running processes of a container |
| docker version | Show the Docker version information |
| docker update --restart unless-stopped $(docker ps -q) | And this [command](https://docs.docker.com/config/containers/start-containers-automatically/) will ensure all currently running containers will be restarted unless stopped |
| docker network ls | List all docker network |
| docker port [ID/NAME] | List container port mapping or run "docker ps" |
| docker-compose up -d | Tells Docker to process the contents of the composite file and configure the specified volumes, networks, and containers |
| docker-compose stop | Tells Docker to stop the contents of the composite file and configure the specified volumes, networks, and containers |
| docker-compose exec [ID/NAME] env | To see what environment variables are available to the web service |
| docker-compose down --volumes | You can bring everything down, removing the containers entirely, with the down command. Pass --volumes to also remove the data volume, if used |
| docker-compose down --volumes --rmi all | You can bring everything down, removing the containers entirely, volumes and images |
| docker-compose logs -f [ID/NAME] | Show container logs continually |
| docker-compose top | Show the running processes |
