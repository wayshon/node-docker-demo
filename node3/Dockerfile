FROM node:8

RUN mkdir -p /opt/app/node3

ARG NODE_ENV=production
ENV NODE_ENV $NODE_ENV
ARG PORT=6003
ENV PORT $PORT
EXPOSE $PORT 6013 6023

WORKDIR /opt/app/node3
COPY package.json /opt/app/node3
RUN npm install && npm cache clean --force

WORKDIR /opt/app/node3
COPY . /opt/app/node3

CMD [ "npm", "start" ]