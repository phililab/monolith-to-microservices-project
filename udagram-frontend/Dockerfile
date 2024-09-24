FROM beevelop/ionic:latest AS ionic

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm ci --force

COPY . .
RUN NODE_OPTIONS=--openssl-legacy-provider ionic build

FROM nginx:alpine

COPY --from=ionic  /usr/src/app/www /usr/share/nginx/html