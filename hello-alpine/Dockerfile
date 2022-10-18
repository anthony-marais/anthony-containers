FROM alpine:3.15.0

#FROM ubuntu:20.04

LABEL version="1.0.0" maintainer="anthony marais" os="ubuntu"

ENV CONTAINER_USER="anthony_marais"

#RUN apt-get update
#RUN apt-get install figlet
RUN apk add figlet


# apk install -y figlet

RUN adduser -D $CONTAINER_USER
USER $CONTAINER_USER

#CMD [echo $USER]
#CMD echo USER
CMD figlet "hello-alpine, I’m "$(whoami)" and this is a container from my first image"
