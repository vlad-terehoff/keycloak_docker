FROM nginx:1.26-alpine
RUN rm /etc/nginx/conf.d/default.conf
COPY ./nginx/nginx.conf /etc/nginx/conf.d
CMD ["nginx-debug", "-g", "daemon off;"]