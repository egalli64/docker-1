# Getting started

This repository is a sample application for users following the getting started guide at https://docs.docker.com/get-started/.

The application is based on the application from the getting started tutorial at https://github.com/docker/getting-started

## Step 1 - setup
- https://docs.docker.com/engine/
- https://docs.docker.com/engine/install/debian/
- https://docs.docker.com/engine/install/linux-postinstall/

### Some useful commands
- sudo service docker {start|stop|restart|status}
- docker run hello-world
- docker ps [-a]
- docker system prune -a # cleanup

## Step 2
- https://docs.docker.com/get-started/workshop/02_our_app/
- After adding the Dockerfile
- docker build -t getting-started .
- docker run -d -p 127.0.0.1:3000:3000 getting-started

See the resulting web app on the browser

## Step 3
- https://docs.docker.com/get-started/workshop/03_updating_app/
- Change a line in src/static/js/app.js
- docker build -t getting-started .
- docker run -dp 127.0.0.1:3000:3000 getting-started

### Some useful commands
- docker stop {id}
- docker rm {id}
- docker rm -f {id}         # stop and remove
- docker system prune -a    # cleanup

## Step 4
- https://docs.docker.com/get-started/workshop/04_sharing_app/
- Log in to https://hub.docker.com/
- Push the "Create a repository" button
- Name it "getting-started", and create it (as public)
- docker tag getting-started {username}/getting-started
- docker login
- docker push {username}/getting-started

### Some useful commands
- docker image ls
- docker image prune -a     # remove all unused images
- docker rmi {id}           # remove an image by id

# Step 5
- https://docs.docker.com/get-started/workshop/05_persisting_data/
- docker volume create todo-db
- docker run -dp 127.0.0.1:3000:3000 --mount type=volume,src=todo-db,target=/etc/todos getting-started
- Add some items in the todo app
- Stop and remove the container
- Start a new container as above, the items persisted

### Some useful commands
- docker volume ls
- docker volume inspect {volume-name}
