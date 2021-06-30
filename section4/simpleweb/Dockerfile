# specify a base image
FROM node:alpine

# set container work directory
WORKDIR /usr/app

# run some commands to install additional programs
COPY ./package.json ./
RUN npm install
COPY ./ ./

# specify a command to run on container startup
CMD ["npm", "start"]