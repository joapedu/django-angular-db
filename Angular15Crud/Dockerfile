FROM node:alpine

LABEL maintainer="João Eduardo Braga <joaoeduardobraga2@gmail.com>"

WORKDIR /app

COPY . .

RUN npm install -g @angular/cli

EXPOSE 8081

CMD [ "ng","serve","--port","8081" ]