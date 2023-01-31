FROM node:latest as angular

LABEL maintainer="João Eduardo Braga <joaoeduardobraga2@gmail.com>" 

WORKDIR /app

COPY package.json /app

# silent to ignoring logs
RUN npm install --silent

COPY . .

RUN npm run build

FROM nginx:alpine

VOLUME /var/cache/nginx

COPY --from=angular app/dist/angular15-crud /usr/share/nginx/html

COPY ./config/nginx.conf /etc/nginx/conf.d/default.conf

# docker build -t teste-angular .
# docker run -p 8081:80 teste-angular
