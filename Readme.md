How to use Docker for trivial tasks

   I was confused a long time with what Docker is and how it works exactly. I am writing this post to help others in similar situation that I was. According to my understanding docker is nothing but a container used to install a bunch of dependencies in a small box, this box is kept apart from your physical computer.

   Consider this: you are following a Tensorflow object-detection tutorial and the instrutor has told you to install Tensorflow 1.2 on your computer. But you have tensorflow 1.7 installed already on your machine and you dont want to downgrade. Docker comes to rescue in this case. Using Docker you can create a container and install all that you need (in this case Tensorflow 1.2). This container will not affect your orignal installation whatsoever.

Start with downloading Docker:
```Download docker from: https://hub.docker.com/editions/community/docker-ce-desktop-mac```

Signup your gmail account with docker. Note that you cannot use Docker if you are not signed in.

First step is to run hello world:

IN
```ajinkyabobade$ docker container run alpine echo "Hello World" ```

OUT
```Unable to find image 'alpine:latest' locally
latest: Pulling from library/alpine
8e402f1a9c57: Pull complete 
Digest: sha256:644fcb1a676b5165371437feaa922943aaf7afcfa8bfee4472f6860aad1ef2a0
Status: Downloaded newer image for alpine:latest
Hello World 
```
Lets analyse the input(IN)

'docker container run': means hey docker be ready to do what I say

'alpine': This is called a container image. Think of it this way when you press Command+Space on MacOS and type 'Terminal' it opens a Terminal, now replace the word 'Terminal' with 'alpine' that is exactly what alpine is.

echo "Hello World": is the command that I should run inside 'alpine'

So to summarise. I opened a new terminal inside docker container and typed the command echo "Hello World" in it


Once you assign a task to 'alpine' remember that you need to stop that task other wise it will unnecessarily consume your system memory. In order to stop the task first list on all the tasks with following command: 

``` docker container ls -a ```

```
CONTAINER ID        IMAGE               COMMAND                CREATED             STATUS                      PORTS               NAMES
cccc42eb6f80        alpine              "echo 'Hello World'"   36 minutes ago      Exited (0) 36 minutes ago                       sharp_noether
caabb8fdd5d0        hello-world         "/hello"               2 hours ago         Exited (0) 2 hours ago                          heuristic_diffie
```

```
docker container rm cccc42eb6f80
```
'docker container rm' will stop it. Tip if its not stopping use: '-f or --force'



