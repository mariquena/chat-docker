# Based on most recent LTS node version, and Alpine Linux
FROM node:14.17.1-alpine
WORKDIR /app
COPY package.json package.json
COPY package-lock.json package-lock.json
RUN npm install
RUN mkdir src
COPY ./src ./src
WORKDIR /app/src
CMD [ "node", "coordinador.js" ]