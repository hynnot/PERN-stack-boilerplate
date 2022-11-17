FROM node:lts
LABEL Tony Morellá Llácer <hynnot@gmail.com>
LABEL repo=https://github.com/hynnot/PERN-stack-boilerplate

FROM node:lts AS builder
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY ./frontend/package.json ./frontend/tsconfig.json ./
COPY ./frontend/src ./src
COPY ./frontend/public ./public
COPY ./types/ /usr/types
RUN npm install
RUN npm build

FROM nginx:stable
COPY --from=builder usr/app/build/ /usr/share/nginx/html
COPY ./frontend/nginx.conf /etc/nginx/conf.d/default.conf
