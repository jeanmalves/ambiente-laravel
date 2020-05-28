FROM nginx:1.15.0-alpine

RUN apk add --no-cache openssl

ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-alpine-linux-amd64-$DOCKERIZE_VERSION.tar.gz

# Remove configuracao padrao que exibe ("welcome nginx")
RUN rm /etc/nginx/conf.d/default.conf

# Copia configuracao do nginx para o container
COPY ./nginx.conf /etc/nginx/conf.d

WORKDIR /var/www
