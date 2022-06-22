FROM node:10-alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./
RUN npm install

COPY server.js server.js

# Exposing the application port
EXPOSE 4000

# Running the application
CMD [ "node", "server.js" ]