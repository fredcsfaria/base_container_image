FROM icr.io/appcafe/ibm-semeru-runtimes:open-11-jre-ubi as semeru
FROM alpine
ENV LANG en_US.UTF-8
ENV JAVA_HOME=/opt/java/openjdk
ENV PATH="${JAVA_HOME}/bin:${PATH}"
COPY --from=semeru $JAVA_HOME $JAVA_HOME
ARG JAR_FILE=target/*.jar
COPY ${JAR_FILE} app.jar

ENTRYPOINT ["java","-jar","/app.jar"]
