FROM node:14.17.1
WORKDIR /app
COPY . .
RUN npm install
WORKDIR /app/src
CMD [ "node", "servidorHTTP.js"]