FROM nginx:1.24.0
RUN rm -rf /var/www/html/*
RUN rm -f /etc/nginx/sites-enabled/default
COPY UI/* /var/www/html/
COPY nginx.conf /etc/nginx/sites-available/roboshop
RUN ln -s /etc/nginx/sites-available/roboshop /etc/nginx/sites-enabled/roboshop

ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
CMD ["node", "server.js"]