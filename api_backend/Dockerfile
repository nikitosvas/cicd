FROM node:alpine


RUN sudo npm config set registry https://registry.npmjs.org/

RUN sudo git clone https://github.com/docker/buildx.git

RUN sudo cd buildx && ./buildx install

RUN sudo npm config set registry https://registry.npmjs.org/

WORKDIR /app

EXPOSE 5000

COPY package*.json /app/

RUN sudo npm install

COPY . .

CMD [ "npm", "run", "dev" ]
