FROM openresty/openresty
RUN apt-get update && apt-get install -y curl

RUN NGINX_CACHE_PURGE_URL=$(curl -s https://api.github.com/repos/magiclen/nginx-cache-purge/releases/latest | sed -r -n 's/.*"browser_download_url": *"(.*\/nginx-cache-purge_'$(uname -m)')".*/\1/p') \
    && curl -L -o /usr/local/bin/nginx-cache-purge $NGINX_CACHE_PURGE_URL \
    && chmod +x /usr/local/bin/nginx-cache-purge


COPY images /usr/share/nginx/html/images
COPY ./servers/nginx-cache-server/nginx.conf /etc/nginx/nginx.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]