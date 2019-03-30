FROM openjdk:8

# alpine version of openjdk wont work because GRPC under TLS cannot work on minified version of glibc library

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JAVA_OPTS="" \
    JHIPSTER_SLEEP=0

VOLUME /tmp
EXPOSE 80

ADD *.jar /app.jar

CMD echo "The application will start in ${JHIPSTER_SLEEP}s..." && \
    sleep ${JHIPSTER_SLEEP} && \
    java ${JAVA_OPTS} -Djava.security.egd=file:/dev/./urandom -jar app.jar
