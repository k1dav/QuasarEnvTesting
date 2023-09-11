FROM node:16-alpine

ARG test
ARG no_test
ENV test ${test} 
ENV no_test ${no_test}

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
