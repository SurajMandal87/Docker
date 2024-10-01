Hello Captain Docker Image
This repository contains a Dockerfile that creates a simple Ubuntu-based Docker image. The image prints "Hello Captain" when run.
Dockerfile Contents
dockerfileCopyFROM ubuntu:latest

RUN apt-get update && apt-get install -y curl

RUN echo "Hello Captain" > /hello.txt

CMD ["cat", "/hello.txt"]
What it does

Uses the latest Ubuntu image as a base
Updates the package list and installs curl
Creates a file /hello.txt with the content "Hello Captain"
Sets the default command to display the contents of /hello.txt

Building the Image
To build the Docker image, run the following command in the directory containing the Dockerfile:
Copydocker build -t hello-captain .
Running the Container
To run the container and see the "Hello Captain" message, use:
Copydocker run hello-captain