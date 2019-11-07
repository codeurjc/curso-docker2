# our base image
FROM maven:3-jdk-8-slim

COPY . /usr/src/app

WORKDIR /usr/src/app

CMD ["mvn", "package"]