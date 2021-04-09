FROM nginx:latest

COPY homework.html /app/homework.html
COPY nginx.conf /etc/nginx/conf.d/nginx.conf

#RUN groupadd -g 1001 test
#RUN useradd -m -u 1001 -g 1001 -s /bin/bash test
#RUN usermod -a -G nginx test
#USER 1001

EXPOSE 8000

