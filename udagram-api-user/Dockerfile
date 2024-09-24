FROM node:13

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm ci --force

COPY .. .
EXPOSE 8080
CMD [ "npm", "run", "prod" ]