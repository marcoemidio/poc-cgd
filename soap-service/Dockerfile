FROM openjdk:8-jdk-alpine
VOLUME /tmp
ARG JAVA_OPTS
ENV JAVA_OPTS=$JAVA_OPTS
ADD target/soap-service-0.0.2-SNAPSHOT.jar soap-service-v0.0.2.jar
EXPOSE 8443
ENTRYPOINT exec java $JAVA_OPTS -jar soap-service-v0.0.2.jar
# For Spring-Boot project, use the entrypoint below to reduce Tomcat startup time.
#ENTRYPOINT exec java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -jar read-file.jar
