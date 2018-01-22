FROM openjdk:8-jdk-alpine
RUN  apk update && apk upgrade && apk add netcat-openbsd
RUN mkdir -p /usr/local/simple-service

ARG JAR_FILE
ADD target/${JAR_FILE} /usr/local/simple-service
ADD src/main/docker/run.sh run.sh
RUN chmod +x run.sh
CMD ./run.sh
