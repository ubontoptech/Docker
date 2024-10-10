Docker (Link:https://drive.google.com/file/d/1Ii9G_VJrlJ6Pxwb0brxEQJFikD6p12OC/view?usp=sharing)

step run docker

-npm install
-npm init
-index.js (https://docs.mikelopster.dev/c/basic/docker/basic)
-node index.js

step Dockerfile

-Dockerfile => 
//////////////////////////////////////////////////////
FROM node:18

WORKDIR /user/src/app

COPY ./package.json ./

RUN npm install

COPY ./index.js ./

EXPOSE 8000

CMD ["node", "index.js"]
//////////////////////////////////////////////////////

-docker build -t node-server . (cmd)
-docker images
-docker run -d -p 8000:8000 node-server
-docker ps
-docker rm -f <name>

-docker run -d -p 8000:8000 --name my-container node-server

VSCode
-docker-compose up -d --build

/////////////////////////////////////////////////////////////////
PostgreSQL
-docker pull postgres
-docker images
-docker run --name postgressql -e POSTGRES_USER=admin -e POSTGRES_PASSWORD=topza1997 -p 5432:5432 -d postgres
-docker ps

DBeaver Community

hub.docker.com

