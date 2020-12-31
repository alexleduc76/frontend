Due to a recent update in the Create React App library, we will need to change how we start our containers.

In the upcoming lecture, you'll need to add the -it flag to run the container in interactive mode:

docker run -it -p 3000:3000 alexleduc/frontend 


## Working example commands for each terminal (be sure to run these commands in the root of your project directory)

### Docker Quickstart (recommended)

docker run -it -p 3000:3000 -v /app/node_modules -v "/e/dev/docker/frontend":/app -e CHOKIDAR_USEPOLLING=true alexleduc/frontend

### GitBash

docker run -it -p 3000:3000 -v /app/node_modules -v "/$(pwd)":/app -e CHOKIDAR_USEPOLLING=true alexleduc/frontend
docker run -it -p 3000:3000-v "/$(pwd)":/app -e CHOKIDAR_USEPOLLING=true alexleduc/frontend
docker run -it -p 3000:3000 -v "/$(pwd)":/app alexleduc/frontend
docker run -it -p 3000:3000 -v /app/node_modules -v "/$(pwd)":/app alexleduc/frontend

docker run -it -p 3000:3000 -v /app/node_modules -v "/e/dev/docker/frontend":/app -e CHOKIDAR_USEPOLLING=true alexleduc/frontend

docker run -it -p 3000:3000 -v /app/node_modules -v /e/dev/docker/frontend:/app -e CHOKIDAR_USEPOLLING=true alexleduc/frontend
docker run -it -p 3000:3000 -v /app/node_modules -v /e/dev/docker/frontend:/app alexleduc/frontend


### PowerShell

docker run -it -p 3000:3000 -v /app/node_modules -v /e/dev/docker/frontend:/app -e CHOKIDAR_USEPOLLING=true alexleduc/frontend


docker build -f Dockerfile.dev . -t alexleduc/frontend


cat ~/dev/docker_password.txt | docker login --username alexleduc --password-stdin