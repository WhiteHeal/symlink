FROM nginx:latest
WORKDIR /home/
COPY . .
RUN rm -rf /usr/share/nginx/html/index.html && ln -s /home/docker/index.html /usr/share/nginx/html/index.html
