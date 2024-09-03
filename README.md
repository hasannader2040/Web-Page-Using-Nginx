# Docker Image Website

## Overview

**Docker Image Website** is a web application designed to demonstrate the use of Docker for containerizing web applications. This project showcases how to build, run, and manage a simple web application inside a Docker container, making it easy to deploy and scale the application in different environments.

## Purpose

The main objective of this project is to provide a practical example of using Docker for containerizing a web application. The project aims to solve common deployment challenges by allowing the application to run consistently across different environments. This is particularly useful in scenarios where the application needs to be deployed in multiple environments (e.g., development, testing, production) without any compatibility issues.

## Features

- **Containerized Web Application**: The entire application runs inside a Docker container, ensuring consistency across different environments.
- **Simplified Deployment**: Easy to deploy using Docker commands, eliminating the need for manual setup.
- **Scalable**: Can be easily scaled by running multiple containers.

## Getting Started

### Prerequisites

Before you begin, ensure you have the following installed on your machine:

- **Docker**: Make sure Docker is installed and running on your machine. You can download Docker from the [official website](https://www.docker.com/get-started).

### Installation

To run this project locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/hasannader2040/docker-image-website.git
     ```

2. **Navigate to the project directory:**

```bash
cd docker-image-website
```
3- **Build the Docker image:**


```bash
docker build -t my-docker-image-website .
```

This command will create a Docker image named **my-docker-image-website** based on the instructions in the **Dockerfile**.

## Running the Application
To run the Docker container, use the following command:

```bash
docker run -p 8080:80 my-docker-image-website
```
The **-p 8080:80** flag maps port 80 inside the Docker container to port 8080 on your local machine. You can access the web application by navigating to http://localhost:8080 in your web browser.


## Usage
Here are some examples of how to use the Docker Image Website:

1 - Access the Web Application:

Open a web browser and go to:


```bash
http://localhost:8080
```
You should see the homepage of the web application.

2- Stopping the Docker Container:

To stop the running container, press CTRL + C in the terminal where the Docker container is running. Alternatively, you can use:

```bash

docker ps  # to get the container ID
docker stop <container_id>
```

## Tools and Technologies

This project utilizes the following tools and technologies:

**Docker**: To create, deploy, and run the application in isolated containers.
**Web Server**: The web application is served using a lightweight web server inside the Docker container.
**HTML/CSS**: Basic front-end technologies used to create the web application's user interface.


## Contributing
Contributions are welcome! Please follow these steps to contribute:

1- Fork the repository.
2- Create a new branch (git checkout -b feature/your-feature-name).
3- Make your changes and commit them (git commit -m 'Add some feature').
4- Push to the branch (git push origin feature/your-feature-name).
5- Open a pull request.


## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgements
Special thanks to [mention any individuals, resources, or tutorials that helped in the creation of this project].







# Docker-Image-Website
 ```bash
$ pwd
$ ls
$ cd Course-Docker # and review files
 ```

# Create a Dockerfile using vim 
 ```bash
$ vim Dockerfile
 ```
# Paste the below into the file

 ```bash
FROM nginx:latest
COPY ./Course-Docker/sample-website /usr/share/nginx/html/
EXPOSE 80
 ```
# Build the image from the Dockerfile and run it publishing port 8080 to be mapped to port 80 on the host
 ```bash
$ docker build -t website .
 ```
 ```bash
$ docker images # to review new image
 ```
 ```bash
$ docker run -it --rm -d -p 3000:80 --name web website
 ```

# >> open in browser to test using port 3000 on the local host.

# commit
 ```bash
docker commit web menamagdyhalem/new-web
 ```
## we need to login first ##
 ```bash
$ docker login
 ```


# push image to docker hub
 ```bash
$ docker push menamagdyhalem/new-web # open the docker hub and review repo
 ```

## pull it agian and run a new container
  ```bash
$ docker run -it --rm -d -p 4000:80 --name new-hub menamagdyhalem/new-web
 ```


![Capture](https://github.com/user-attachments/assets/82c90156-c1d9-418a-b7d0-91cd27f9737f)
![docker](https://github.com/user-attachments/assets/b7f2c59c-33be-4bd9-ad2a-8ac2e730492b)

