FROM node:8.16.0-alpine as node
FROM openjdk:8-jre-alpine
MAINTAINER himanoa <matsunoappy@gmail.com>
COPY --from=node /usr/local/bin/node /usr/local/bin/
COPY --from=node /usr/local/bin/npm /usr/local/bin/
COPY --from=node /usr/local/lib/* /usr/local/lib/
RUN wget -P /usr/local/lib https://dl.google.com/devsite/firestore/cloud-firestore-emulator.jar
RUN apk add git
