FROM node:14.17-alpine as build

WORKDIR /app

COPY package.json /app/requirements
COPY package-lock.json /app/requirements

RUN npm install

COPY ./src/App.js /app/src/App.js 
COPY ./src/index.js /app/src/index.js 

CMD ["npm", "start"]