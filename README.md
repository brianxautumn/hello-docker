# hello-docker
Hello world in node, with docker
## Getting Started
Make sure you have docker installed on your local system. Test to see if you have output from the following command. Also install node.
```
$ docker -v
```
```
$ node -v
```
## Node hello world with express
To install express, already included in the package run:
```
npm install
```
Then run the basic app.
```
node index.js
```
And now you can visit localhost:3000 and you should see something like
> Hello World! You have visited this app x times!

## Dockerfile
The Dockerfile contains the necessary setup for running this app from scratch. In this case, just running `npm install` and then copying output to the main app directory inside the container.

## Building
```
$ docker build -t hello-docker .
```
Then check the images to make sure it is built.
```
$ docker image ls
```

## Running
Use docker run, plus the -p flag to map a port. The port maps your local port to the internal docker port. In this case, they are the same.
```
$ docker run -p 3000:3000 hello-docker
```
To see which containers are running, from another terminal.
```
$ docker container ls
```
Then stop it with:
```
$ docker stop <container id>
```
