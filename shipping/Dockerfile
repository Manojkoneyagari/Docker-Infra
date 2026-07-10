FROM maven:3.9.16
WORKDIR /app
COPY src ./src
COPY pom.xml .
RUN mvn clean package
RUN mv target/shipping-1.0.jar shipping.jar 
EXPOSE 8080
ENV CART_ENDPOINT=cart:8080 \
    DB_HOST=mysql

CMD ["java", "-jar", "shipping.jar"]