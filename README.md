# docker-image-website

$ pwd
$ ls
$ cd Course-Docker # and review files


# Create a Dockerfile using vim 
$ vim Dockerfile

# Paste the below into the file
FROM nginx:latest
COPY ./Course-Docker/sample-website /usr/share/nginx/html/
EXPOSE 80

# Build the image from the Dockerfile and run it publishing port 8080 to be mapped to port 80 on the host

$ docker build -t website .

$ docker images # to review new image

$ docker run -it --rm -d -p 3000:80 --name web website

# >> open in browser to test using port 3000 on the local host.

# commit
docker commit web menamagdyhalem/new-web

## we need to login first ##
$ docker login

# push image to docker hub
$ docker push menamagdyhalem/new-web # open the docker hub and review repo


## pull it agian and run a new container 
$ docker run -it --rm -d -p 4000:80 --name new-hub menamagdyhalem/new-web
