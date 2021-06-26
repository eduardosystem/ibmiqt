FROM node:12-alpine
RUN apk update && apk upgrade && \
    apk add --no-cache bash git openssh
WORKDIR /usr/src/app
RUN git clone https://github.com/arcmop/retobase-nodejs.git
WORKDIR /usr/src/app/retobase-nodejs
# Instalando mysql
RUN npm install --save
RUN npm install mysql
EXPOSE 4000
# Iniciando el Node
CMD [ "npm", "start" ]
