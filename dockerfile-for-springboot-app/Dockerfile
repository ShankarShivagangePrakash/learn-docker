FROM eclipse-temurin:8-jdk

ARG SPRING_PROFILE=ed
LABEL author="Shankar"
LABEL email="Shankar@gmail.com"

EXPOSE 8080

COPY target/tomcat-war-app-0.0.1-SNAPSHOT.jar deploy.jar

ENV JAVA_OPTS="-Dspring.profiles.active=dev"

CMD ["java", "-Dspring.profiles.active=${SPRING_PROFILE}", "-jar", "deploy.jar"]