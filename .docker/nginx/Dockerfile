FROM nginx:1.15.0-alpine

# Remove configuracao padrao que exibe ("welcome nginx")
RUN rm /etc/nginx/conf.d/default.conf

# Copia configuracao do nginx para o container
COPY ./nginx.conf /etc/nginx/conf.d
