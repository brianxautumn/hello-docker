# hello-docker
Hello world in node, with docker

## Building
```
$ docker build -t hello-docker .
```

## Running
Use docker run, plus the -p flag to map a port. The port maps your local port to the internal docker port. In this case, they are the same.
```
$ docker run -p 3000:3000 hello-docker
```