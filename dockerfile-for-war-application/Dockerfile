FROM tomcat:8.5.98-jdk8-temurin

LABEL author="Shankar"
LABEL email="Shankar@gmail.com"

EXPOSE 8080

RUN rm -rf ./webapps/*

COPY tomcat-war-app-0.0.1-SNAPSHOT.war /usr/local/tomcat/webapps/ROOT.war

ENV JAVA_OPTS="-Dspring.profiles.active=dev"

CMD ["catalina.sh", "run"]