# 🐳 Hello Captain Docker Image

This repository contains a Dockerfile that creates a simple Ubuntu-based Docker image. The image prints "Hello Captain" when run.

## 📋 Dockerfile Contents

dockerfile
FROM ubuntu:latest

RUN apt-get update && apt-get install -y curl

RUN echo "Hello Captain" > /hello.txt

CMD ["cat", "/hello.txt"]


## 🚀 What it does

1. Uses the latest Ubuntu image as a base
2. Updates the package list and installs `curl`
3. Creates a file `/hello.txt` with the content "Hello Captain"
4. Sets the default command to display the contents of `/hello.txt`

## 🏗️ Building the Image

To build the Docker image, run the following command in the directory containing the Dockerfile:

`bash`
`docker build -t hello-captain .`


## 🏃‍♂️ Running the Container

To run the container and see the "Hello Captain" message, use:

bash
docker run hello-captain


## 📝 Notes

- This image installs `curl`, which can be used for network-related operations if needed.
- The image size may be larger than necessary for such a simple operation due to using the full Ubuntu image and installing `curl`. For a production environment, you might want to optimize this.

## 🌟 Star Us!

If you find this project useful, please consider giving it a star on GitHub! ⭐

## 📞 Contact

If you have any questions or feedback, please open an issue on this repository.

---

Made with ❤️ by [Your Name/Organization]
