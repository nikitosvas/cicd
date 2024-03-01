FROM node:alpine

RUN git clone https://github.com/docker/buildx.git

RUN sudo cd buildx && ./buildx install

WORKDIR /app

EXPOSE 3000

COPY package*.json /app/

RUN npm install

COPY . .

CMD [ "npm", "run", "dev" ]


