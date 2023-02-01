FROM node:latest as node

LABEL maintainer="João Eduardo Braga <joaoeduardobraga2@gmail.com>" 

WORKDIR /app

COPY . .

# silent to ignoring logs
RUN npm install --silent

RUN npm run build

FROM nginx:alpine

COPY --from=node /app/dist/angular15-crud /usr/share/nginx/html

EXPOSE 8081