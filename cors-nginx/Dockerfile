#++++
FROM nginx:stable-alpine

# Копируем конфиг и директорию с include
COPY nginx.conf /etc/nginx/nginx.conf
COPY conf.d /etc/nginx/conf.d

# (опционально) копируем статический контент
# COPY html /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]