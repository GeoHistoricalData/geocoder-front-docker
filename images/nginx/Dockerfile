FROM nginx:1.12

RUN apt-get update && \
    apt-get install -y git


RUN git clone  https://github.com/GeoHistoricalData/geocoder-front.git /var/www/geocoder

RUN rm /etc/nginx/conf.d/default.conf

COPY include/nginx.conf /etc/nginx/conf.d/geocoder.conf




