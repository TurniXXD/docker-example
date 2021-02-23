# docker-example
run git push after everything is done: git push -u origin master

https://www.youtube.com/watch?v=fqMOX6JJhGo&ab_channel=freeCodeCamp.org

install and start docker
test image can be whalesay for running this use this command:

$ docker run docker/whalesay cowsay boo

# Quicklist of docker commands
run latest version image / container:
$ docker run

list containers:
$ docker ps [-a]

stop a container:
$ docker stop [ASSIGNED NAME]

remove a container:
$ docker rm [ASSIGNED NAME]

list images:
$ docker images

remove image:
$ docker rmi [IMAGE NAME]

for downloading an image and not running the container straightaway:
$ docker pull [IMAGE NAME]

append a command e.g. sleep:
$ docker run [IMAGE NAME] sleep 5

execute a command on a running container:
$ docker exec [ASSIGNED NAME] [COMMAND ON CONTAINER]

run docker container in detach mode (on background):
$ docker run -d [ASSIGNED NAME]

then for attaching docker container again run:
$ docker attach [FIRST FEW SYMBOLS OF CONTAINER ID FROM DETACH COMMAND]

run specified version of an image:
$ docker run [IMAGE NAME]:[SPECIFIED VERSION]

run app in interactive mode with sudo terminal (can handle inputs and terminal commands):
$ docker run -it [APP NAME]

map port e.g. 5000 to e.g. 80 for remote user to access internal container of docker host:
$ docker run -p 80:5000 [APP NAME]

map data from running instance to another container (e.g. when you want to delete container but want to keep the data):
$ docker run -v [NEW CONTAINER]:[OLD CONTAINER] [IMAGE NAME]

inspect container (detailed info about container):
$ docker inspect [ASSIGNED NAME]

get container logs (e.g. when it is in detach mode):
$ docker logs [ASSIGNED NAME]

you can declare env var in your code (e.g. in python: [VAR NAME] = os.environ.get('ENV VAR NAME')) and be able to set it when running your docker app with:
$ docker run -e [ENV VAR NAME]=[NEW VALUE] [APP NAME]
you can then inspect this env var with docker inspect

# Create your own image 
Use Dockerfile in this repo or create your own

build your Dockerfile with:
$ docker build Dockerfile -t [PATH WHERE YOU WILL CREATE YOUR IMAGE]

to make your image available on docker.hub registry run this push command:
$ docker push [PATH TO YOUR IMAGE]









