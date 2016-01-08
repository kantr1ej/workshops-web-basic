# Hack@UCF Web Workshops - Basic Category

This is a containerized challenge set for the "basic" category in Hack@UCF's web application security workshops. For workshop attendees, welcome! Read the instructions below to get started.

## Instructions

The recommended way to use this repository is to run this on your computer using Docker. This is easiest on a computer running OS X or Linux, but should be doable using Windows. You must have git installed.

Here are the commands to copypaste under OS X or Linux:

```
git clone https://github.com/mark-ignacio/workshops-web-basic.git
cd workshops-web-basic
sudo docker build -t workshop-basic . && sudo docker run -it --rm --name basic workshop-basic
```

Press Ctrl+C on the terminal to stop the server.
