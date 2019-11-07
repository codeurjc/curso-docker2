# our base image
FROM maven:3-jdk-8-slim as builder

WORKDIR /usr/src/app
COPY pom.xml .
RUN mvn dependency:go-offline

COPY . /usr/src/app
RUN mvn package

FROM openjdk:8-jre
COPY --from=builder /usr/src/app/target/*.jar /usr/app/app.jar
WORKDIR /usr/app
CMD [ "java", "-jar", "app.jar" ]  