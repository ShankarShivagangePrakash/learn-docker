Creating a GitHub repository to practice and document my Docker learnings.

Basic command: 

Build Docker Image: docker build -t <image_name>

Run Docker image in a container: docker run -p <public_port>:8080 <image_name>

/****************/

Created a simple dockerfile to build docker image for a jar file.
    
    docker build command: docker build -t <image_name> .

    docker run command: docker container run -p <public_port>:8080 <image_name>

/****************/

 Deploy war file to docker container.
    
    Dockerfile, pull tomcat-image for a particular java version.
    Tomcat default files will be there in webapss folder.
    Remove them and place your war file in that location.
    So that will be rendered.
    
    Docker build command: docker build -t tomcat-war-app .
    
    Docker container run command: docker container run -p 80:8080 tomcat-war-app

/****************/

Deploy spring-boot-application to docker container.

    ARG parameter is used to accept argument for dockerfile.

    Docker build command:
    docker build -t spring-boot-image --build-arg SPRING_PROFILE=dev .

    Docker container run command:
    docker container run -p 80:8080 -e SPRING_PROFILE=dev spring-boot-image

/****************/