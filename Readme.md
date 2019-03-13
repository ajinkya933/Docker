How to use Docker for trivial tasks

I was confused a long time with what Docker is and how it works exactly. I am writing this post to help others in similar situation that I was. According to my understanding docker is nothing but a container used to install a bunch of dependencies in a small box, this box is kept apart from your physical computer.

Consider this: you are following a Tensorflow object-detection tutorial and the instrutor has told you to install Tensorflow 1.2 on your computer. But you have tensorflow 1.7 installed already on your machine and you dont want to downgrade. Docker comes to rescue in this case. Using Docker you can create a container and install all that you need (in this case Tensorflow 1.2). This container will not affect your orignal installation whatsoever.

Start with downloading Docker:
Download docker from: https://hub.docker.com/editions/community/docker-ce-desktop-mac
