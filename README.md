# Hack@UCF Web Workshops - Basic Category

This is a containerized challenge set for the "basic" category in Hack@UCF's web application security workshops. For workshop attendees, welcome! Read the instructions below to get started.

## Instructions

The recommended way to use this container is to run this on your computer using Docker. This is easiest on a computer running OS X or Linux, but should be doable using Windows. You must have git installed.

### OS X

**NOTE**: These instructions are a little complicated and will only make complete sense to someone who already knows both Docker and bash. Please ask for help if this does not work.

Install the official [Docker Toolbox](https://docs.docker.com/engine/installation/mac/#installation) for OS X and open the Docker Quickstart Terminal.

Please take note of your Docker Machine VM's IP address, since that IP is how you will access the web server. Run this command to find out:

```
$ echo $DOCKER_HOST
tcp://192.168.99.101:2376
```

For the example above, you will access the webserver by going to `http://192.168.99.101`. Change the IP address to whatever you get on your machine.

```
$ git clone https://github.com/mark-ignacio/workshops-web-basic.git
$ cd workshops-web-basic
$ docker build -t workshop-basic .
$ docker run -it --rm -v $(pwd)/src:/var/www/html -p 0.0.0.0:80:80 --name basic workshop-basic
```

Navigate to `http://localhost` to see the contents of the src directory.


### Linux

Install the docker package for whatever distribution you're using.

```
$ git clone https://github.com/mark-ignacio/workshops-web-basic.git
$ cd workshops-web-basic
$ sudo docker build -t workshop-basic .
$ sudo docker run -it --rm -v $(pwd)/src:/var/www/html -p 127.0.0.1:80:80 --name basic workshop-basic
```

Navigate to `http://localhost` to see the contents of the src directory.

## Run instructions

Press Ctrl+C on the terminal to stop the container. Re-run the last line you copied (the one that has `docker run`) to start the server again!

You should be able to modify files in the `src` directory and have them take effect on the webserver. **Use this to test your changes and show workshop staff your solution!**
