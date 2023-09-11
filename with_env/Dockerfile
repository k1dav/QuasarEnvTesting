FROM node:16-alpine

ENV test null
ENV no_test null
RUN env

WORKDIR /workspace
COPY . .

RUN yarn global add @quasar/cli \
    && yarn \
    && quasar build

FROM nginx

WORKDIR /var/www/html

COPY ./nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=0 --chown=www-data:www-data /workspace/dist/spa .
