# Hack@UCF Web Workshops - Basic Category

This is a containerized challenge set for the "basic" category in Hack@UCF's web application security workshops. For workshop attendees, welcome! Read the instructions below to get started.

## Instructions

The recommended way to use this container is to run this on your computer using Docker. This is easiest on a computer running OS X or Linux, but should be doable using Windows. You must have git installed.

### OS X and Windows

**NOTE**: These instructions are relatively complicated and will only make complete sense to someone who already knows both Docker and bash. Please ask for help if this does not work.

Install the official Docker Toolbox [for OS X](https://docs.docker.com/engine/installation/mac/#installation) or [for Windows](https://docs.docker.com/engine/installation/windows/#requirements). For Windows, please read the requirements section first to ensure you can run Docker. If you cannot, please talk to one of workshop staff.

Open the Docker Quickstart Terminal and wait until the first-start process is complete.

Please take note of your Docker Machine VM's IP address, since that IP is how you will access the challenges! Run this command to get it:

```
$ echo $DOCKER_HOST
tcp://192.168.99.101:2376
```

For the example above, you will access the webserver by going to `http://192.168.99.101`. Change the IP address to whatever you get on your machine.

```
$ git clone https://github.com/mark-ignacio/workshops-web-basic.git
$ cd workshops-web-basic
$ docker build -t workshop-basic .
```

On OS X, run:

```
$ docker run -it --rm -v $(pwd)/src:/var/www/html -p 0.0.0.0:80:80 --name basic workshop-basic
```

On Windows, run: (note the extra slash before `$(pwd)`)

```
$ docker run -it --rm -v /$(pwd)/src:/var/www/html -p 0.0.0.0:80:80 --name basic workshop-basic
```

Now you can navigate to `http://DOCKER.HOST.IP.HERE` to see the contents of the src directory.


### Linux

Install the docker and git packages for whatever distribution you're using.

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
