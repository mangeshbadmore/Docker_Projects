FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

##VOLUME [ "/app/data/feeback" ]        //This creates Anonymous volume and it gets deleted when ctr is removed (not stopped alone). To make keep volumes persistent, we will create a vooume at runtime and mount it on ctr using -v VOLUME_NAME:MOUNT_POINT 

EXPOSE 80

CMD [ "node", "server.js" ]