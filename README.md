# Getting started

This repository is a sample application for users following the getting started guide at https://docs.docker.com/get-started/.

The application is based on the application from the getting started tutorial at https://github.com/docker/getting-started

## Setup
- https://docs.docker.com/engine/
- https://docs.docker.com/engine/install/debian/
- https://docs.docker.com/engine/install/linux-postinstall/

## Some useful initial commands
- service docker {start|stop|restart|status}
- docker run hello-world
- docker ps [-a]
- docker stop {id}
- docker system prune -a # cleanup

## Step 1
- https://docs.docker.com/get-started/workshop/02_our_app/
- After adding the Dockerfile
- docker build -t getting-started .
- docker run -d -p 127.0.0.1:3000:3000 getting-started

See the resulting web app on the browser
