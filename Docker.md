start a container: docker run nginx
list containers: docker ps -a
stop container : docker stop silly_sammet
remove container : docker rm silly_sammet
list images : docker images
remove images : docekr rmi nginx
download image : docker pull nginx
start sleep process in not running container : docker run ubuntu sleep 5
start process in an already running container : docker exec distracted_mcclintock cat /etc/hosts
run container in attach mode (now in terminal) : docker run kodekloud/simple-webapp
run container in detach mode (running in background) : docker run -d kodekloud/simple-webapp
reattach detached container : docker attach a043d
run older version image on a container using tag  : docker run redis:4.0
container with input field with result : docker run -it kodekloud/simple-prompt-docker 
mapping port from container to webserver for direct access(browser access port:container port) : docker run -p 80:5000 kodekloud/simple-webapp
persistant directory : dpcker run -v /opt/datadir:/var/lib/mysql mysql
show details on a container : docker inspect blissful_hopper
show docker log : docker logs blissful_hopper
add environment variable : docekr run -e APP_COLOR=green simple-webapp-color

CREATE IMAGE
============================

FROM ubuntu

RUN apt-get ubuntu
RUN apt-get install python
RUN pip install flask
RUN pip install flask-mysql


COPY . /opt/source-code

ENTRYPOINT FLASK_APP=/opt/source-code/app.py flask run

ENTRYPOINT ["sleep"]

CMD ["sleep", "5"]


docker  uild Dockwrfile -t mmumshad/my-custom-app
docker push mmumshad/my-custom-app
docker build Docekrfile -t mmumshad/my-custom-app



