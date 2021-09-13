# Docker

```
docker images
docker ps
docker ps -a
docker ps -aq

docker build -t hello-world .
docker run hello-world
docker run --name Hello hello-world
docker run --name Hello -d hello-world
docker rm $(docker ps -aq)
docker stop Hello
docker rm Hello
docker run --name Hello -d --rm hello-world

python3 -m pip install 'flask'
docker build -t web-app .
docker run --rm --name Web web-app
docker run --rm --name Web -p 80:8080 web-app
docker run --rm --name Web -p 80:8080 -e TZ=Europe/Moscow -v /Users/kostiushenko/github/Docker/resources:/usr/src/app/resources web-app
docker volume ls
docker volume create web
docker run --rm --name Web -p 80:8080 -e TZ=Europe/Moscow -v web:/usr/src/app/resources web-app
docker run --rm -d -p 27017:27017 mongo
docker stop f79422acbcee
docker rmi mongo
docker images
docker images -q
docker rmi $(docker images -q)

docker-compose version
echo "$SHELL"
docker-compose up -d
docker ps
docker-compose down
cd Flask/
docker build -t kostiushenko/flask .
docker login
docker push kostiushenko/flask
```
