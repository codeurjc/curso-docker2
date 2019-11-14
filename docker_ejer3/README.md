docker run --rm -p 8080:8080 -v "$PWD":/usr/src/app/ -w /usr/src/app openjdk:8 java -jar despliegue_ejem1-0.0.1.jar

docker run --rm -p 8080:8080 -it -v "$PWD":/usr/src/app/ -w /usr/src/app openjdk:8 bash