FROM ubuntu:latest

LABEL author="shankar"
LABEL emai="shankar@gmail.com"

RUN apt-get update && apt-get install -y openjdk-8-jdk

WORKDIR /usr/local/bin

COPY test-program.jar .

CMD ["java", "-jar", "test-program.jar"]
