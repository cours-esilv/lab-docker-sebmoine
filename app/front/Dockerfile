FROM nginx:latest
WORKDIR /app

COPY ./index.html /usr/share/nginx/html/index.html
COPY ./style.css /usr/share/nginx/html/style.css
COPY ./entrypoint.sh /usr/local/bin/
RUN chmod +x /usr/local/bin/entrypoint.sh

ENV WS_BACK_URL=http://localhost:8080

EXPOSE 80
ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]