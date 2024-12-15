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
- docker stop <id>
- docker rm <id>
- docker rm -f <id>         # stop and remove
- docker system prune -a    # cleanup
