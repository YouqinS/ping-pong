FROM openjdk:18-ea-11-jdk-alpine
EXPOSE 8080

ARG JAR_FILE=target/pingpong-0.0.1-SNAPSHOT.jar
ADD ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]