# our base image
FROM maven:3-jdk-8-slim

WORKDIR /usr/src/app
COPY pom.xml .
RUN mvn dependency:go-offline

COPY . /usr/src/app
RUN mvn package