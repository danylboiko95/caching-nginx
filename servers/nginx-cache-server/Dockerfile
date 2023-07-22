FROM nginx:1.21.3
# # FROM openresty/openresty:alpine

# # RUN apt-get update && apt-get install nginx-module-lua
# # RUN apt-get install -y libnginx-mod-http-lua
# # RUN apk add --no-cache nginx-mod-http-lua
RUN apt-get update && apt-get install -y nginx-extras

COPY images /usr/share/nginx/html/images
COPY ./servers/nginx-cache-server/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]

# FROM openresty/openresty:1.21.4.1-0-alpine
# COPY images /usr/local/openresty/nginx/html/images
# COPY ./servers/nginx-cache-server/nginx.conf /usr/local/openresty/nginx/conf/nginx.conf
# EXPOSE 80
# CMD ["/usr/local/openresty/bin/openresty", "-g", "daemon off;"]


# FROM openresty/openresty:1.21.4.1-0-alpine-apk
# WORKDIR /usr/local/openresty/nginx/
# # COPY ./servers/nginx-cache-server/nginx.conf /usr/local/openresty/nginx/conf/nginx.conf
# EXPOSE 80
# CMD ["/usr/local/openresty/nginx/sbin/nginx", "-g", "daemon off;"]

