# Based on:
# https://github.com/IsraelHikingMap/graphhopper-docker-image-push/blob/main/Dockerfile

FROM maven:3.6.3-jdk-8 as build
RUN apt-get install -y wget
WORKDIR /graphhopper
COPY ./graphhopper .
RUN mvn clean install

FROM openjdk:11.0-jre
ENV JAVA_OPTS ""
ENV TOOL_OPTS ""
RUN mkdir -p /data
WORKDIR /graphhopper
COPY --from=build /graphhopper/web/target/graphhopper*.jar ./
COPY ./config.yml ./
VOLUME [ "/data" ]
EXPOSE 8989
HEALTHCHECK --interval=5s --timeout=3s CMD curl --fail http://localhost:8989/health || exit 1
