FROM mcr.microsoft.com/openjdk/jdk:11-mariner
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
