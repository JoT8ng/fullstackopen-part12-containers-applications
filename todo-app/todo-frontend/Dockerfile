FROM node:16 AS build-stage

USER node

WORKDIR /usr/src/app

COPY --chown=node:node . .

RUN npm ci

RUN npm run build

RUN npm install -g serve

CMD ["serve", "build"]