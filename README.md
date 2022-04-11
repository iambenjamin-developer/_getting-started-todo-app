# _getting-started-todo-app
https://docs.docker.com/get-started/02_our_app/

DockerFile
```
# syntax=docker/dockerfile:1
FROM node:12-alpine
RUN apk add --no-cache python2 g++ make
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
```

Construir imagen
```
 docker build -t getting-started .
```

Correr imagen
```
 docker run -dp 3000:3000 getting-started
```
