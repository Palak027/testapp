# Test Node App - Dockerized

# This is a simple Node.js app that has been containerized using Docker.

# Explaining Docker file

**FROM node** 

- we are using official node image as base image. This image include Node.js and npm, which are essential for running a Node.js application.

**WORKDIR /myapp** 
- this sets the working directory inside the container to '/myapp'.

**COPY . .**
- this command copy everything in your working directory which you assings above

**RUN npm install**
- as for node application its mandatory have node modules to be there so need to run this command

**EXPOSE 3000**
- This tell Docker that application will listen on port 3000inside the container.

**CMD ["npm", "start"]**
- this command defines the default behaviour of the container when its start.

## **How to Build image**

docker build -t <imagename> . 

## how to run a container

docker run -it -d -p 3000:3000 myimage