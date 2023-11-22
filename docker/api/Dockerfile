FROM openjdk:8-jdk
RUN apt-get update && \
    apt-get install -y build-essential
WORKDIR /usr/src/app
COPY . .
RUN cd c && \
    make
RUN cd java && \
    ./gradlew build
EXPOSE 8080
CMD ["java", "-jar", "path/to/java/application.jar"]
