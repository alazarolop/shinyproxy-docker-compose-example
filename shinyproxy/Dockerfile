FROM openjdk:20

COPY shinyproxy /opt/shinyproxy
WORKDIR /opt/shinyproxy/

ENV SP_RELEASE 3.0.1
RUN curl -L -o shinyproxy.jar \
  "https://github.com/openanalytics/shinyproxy/releases/download/v$SP_RELEASE/shinyproxy-$SP_RELEASE.jar"

COPY application.yml application.yml

CMD ["java", "-jar", "/opt/shinyproxy/shinyproxy.jar"]
