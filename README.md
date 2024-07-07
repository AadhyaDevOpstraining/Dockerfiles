#Install Ubuntu

#sudo apt-get update
#sudo apt-get install curl -y
#curl -fsSL get.docksal.io | bash
#sudo usermod -aG docker ubuntu

sudo docker images 	                  --it will list all images that are locally stored with the docker engin
sudo docker image ls 									--it will list all images that are locally stored with the docker engin 
===============================
sudo docker login -u userid -p  password 

sudo docker images                 ---> to see docker images
sudo docker pull hello-world       ---> to pull hello
sudo docker image imagename        ---> it will give perticularimage details 
sudo docker images -q 			       ---> it will display docker imagesid id only

sudo docker rmi  imagename /imageid         ---> it will delete images
sudo docker rmi -f imagename/imageid        ----> with image id also we can remove or forcely delete imagename 

sudo docker images                          ----> check hello-world image avilable (it will downlode from docker hub)

sudo docker container ls --all              ----> it will list all the containers
sudo docker run hellow-world                ----> check hellow world container is created or not
sudo docker container ls                    ----> it will list the containers
sudo docker rm containerid                  ----> it will delete container
sudo docker rm -f containername             ----> it will delete forcefully containers  
 
sudo docker rmi hello-world                 ----> it will delete images
sudo docker rmi -f  hello-world             ---->  forcely it will delete image

======================
sudo docker ps 
sudo docker container ls                     ---> list running container and 
sudo docker container ls -a                  --->it will not list stopped containers)
=======================
sudo docker ps -a                            ---> it will list only stoped containers
sudo docker container ls --all
sudo docker container -a                     ---> it will list all contaisers (stoped and start both will display)
===============================
Docker container stop/start

sudo docker stop <containername/id>
sudo docker container stop  <containername/id>
sudo docker kill < containerid/name>   ---> it will kill the containers means just it will stop the container 

sudo docker start <container name/id>
sudo docker container start <containerid>

sudo docker stop $(docker ps -a -q)   ---> it will stop all the container
sudo docker rm -f $(docker ps -aq)    ---> delete all running and stoped containers 
sudo docker container prune    ---> it will Delete all stoped containers 

sudo docker ps -a|awk '$2=="hello-world" {print $1 |xargs docker rm   ---> it will  delete all the containers related hello-world image

sudo docker pause containerid/name    --->it will pause the container
sudo docker unpause containerid/name  ---> it will unpause the container

docker container status are one of below 

crated, restarting, running, removing,paused,exited, or dead.



sudo docker ps -a --filter "name=Aadhyamai technologies"  --->it will display container with name Aadhyamai technologies

sudo docker ps -a --filter 'exited=0'
sudo docker ps --filter status=running
sudo docker ps --filter status=


sudo logs <container-name>              ---> it will display the logs for that container.
sudo logs --tail 100 <container name>   ---> print the last 100 lines of a container's logs 

sudo docker top containerid/name     ----> this will shows the top processes with in a containers


sudo docker rename <container old Name> <container new name>  --> it will rename the container
===================================
docker search command will work only if server is conneted to Internet then only it will work  
sudo docker search puppet
sudo docker search tomcat
sudo docker search wildfily
sudo docker search ubuntu
sudo docker search linux
====================================
sudo docker ps -a
sudo docker ls 
sudo docker container ls -a                                         --- to chek stoped containers list
sudo docker rm $ (docker ps -aq )                                   --it will deleat containers along with ids 
sudo docker rm -f dockerID                                          -- it will deleat permanently 
sudo docker login -u mallikarjuna89 -p gpkr1989 

sudo docker run hello-world 
sudo docker images 
  or 
  
sudo docker pull hello world 
docker images
docker ps 
docker run hellow-world 
=============================================
uplode docker files 

sudo apt-get install zip
sudo apt-get install unzip

sudo docker 

sudo docker build -f  Dockerfile .

naralamalli2@docker:~/Dockerfiles$ sudo docker images
REPOSITORY            TAG                 IMAGE ID            CREATED             SIZE
<none>                <none>              94df119ea2f1        20 seconds ago      64.2MB

=================================================

Docker files
docker build -f Dockerfile_Tomcat .
docker images 
docker build -t devops .

====================================================================
tomcat and wildfliy 

sudo docker images 

sudo docker build -f Dockerfile_Wildfly -t wildfilyimage .

sudo docker images

sudo docker build -f Dockerfile_Wildfly -t mallikarjuna89/wildfilyimage .

sudo docker push mallikarjuna89/wildfilyimage

sudo docker ps
 
sudo docker rm d699ef991a6f
 
sudo docker run -p 8090:8080 -d --name wildfilycontainer wildfilyimage 
 
sudo docker exec -it wildfilycontainer /bin/bash
 
cd wildfly/
cd bin/
ls -l 
sh add-user.sh
a
 
 
sudo docker run -p 8090:8080 -p 9990:9990 -d --name wildfilycontainer wildfilyimage (wildfliy admin port mapping )
========================================================================
