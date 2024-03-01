FROM node:alpine


RUN npm config set registry https://registry.npmjs.org/

RUN git clone https://github.com/docker/buildx.git

RUN cd buildx && ./buildx install

WORKDIR /app

EXPOSE 5000

COPY package*.json /app/

RUN npm install

COPY . .

CMD [ "npm", "run", "dev" ]
