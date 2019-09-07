# Introduction

How to use Docker for trivial tasks

   I was confused a long time with what Docker is and how it works exactly. I am writing this post to help others in similar situation that I was. According to my understanding docker is nothing but a container used to install a bunch of dependencies in a small box, this box is kept apart from your physical computer.

   Consider this: you are following a Tensorflow object-detection tutorial and the instrutor has told you to install Tensorflow 1.2 on your computer. But you have tensorflow 1.7 installed already on your machine and you dont want to downgrade. Docker comes to rescue in this case. Using Docker you can create a container and install all that you need (in this case Tensorflow 1.2). This container will not affect your orignal installation whatsoever.

## Download Docker 

I used Digital Ocean to download docker on ubuntu 18.0: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04


## Pulling a image

I want to pull image from https://github.com/tesseract-ocr/tesseract/wiki/4.0-Docker-Containers . I used

```docker pull mylamour/tesseract-ocr:opencv```

## Running image 

I referred https://stackoverflow.com/questions/18497688/run-a-docker-image-as-a-container to run this image:

### Step1: Get Image ID

```
docker images

REPOSITORY               TAG                 IMAGE ID            CREATED             SIZE
mylamour/tesseract-ocr   opencv              f496446c0f47        2 years ago         3.35GB
```
### Step2: Run

```docker run -i -t f496446c0f47 /bin/bash```

