FROM ubuntu:16.04

WORKDIR /usr/src/app

RUN apt-get update -y && apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5000
CMD ["npm", "start"]