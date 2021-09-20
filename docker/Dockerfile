FROM node:14.15.0-alpine3.12 as base
LABEL maintainer "Cute_Wisp <sweatpotato13@gmail.com>"
COPY ./package.json ./
COPY ./lerna.json ./
COPY ./tsconfig.json ./
COPY ./packages/ ./packages
RUN yarn install --frozen-lockfile
RUN yarn build

CMD ["yarn", "start:prod"]