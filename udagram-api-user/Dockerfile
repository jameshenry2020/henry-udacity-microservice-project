FROM node:12
# Create app directory
WORKDIR /usr/src/app

LABEL maintainer="henry2techgroup@gmail.com"
LABEL decription="Development image for udagram microservice Project"
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied where available (npm@5+)
COPY package*.json ./

#for local development
#RUN npm install
# If you are building your code for production
RUN npm ci 
# Bundle app source
COPY . .

EXPOSE 8080

CMD [ "npm", "run", "prod" ]