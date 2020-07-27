FROM ubuntu:20.04
LABEL MAINTAINER="Digitalis <info@digitalis.io>"
ENV LANG C.UTF-8
RUN apt-get update && apt-get upgrade -y && apt-get install python2 -y
ADD http://apache.mirror.anlx.net/cassandra/3.11.7/apache-cassandra-3.11.7-bin.tar.gz /cassandra.tar.gz
WORKDIR /
RUN tar zxf /cassandra.tar.gz && mv /apache-cassandra* /cassandra && \
    rm -f /cassandra.tar.gz && rm -r /cassandra/doc /cassandra/javadoc /cassandra/conf /cassandra/interface
#ENTRYPOINT [ "/cassandra/bin/cqlsh", "--cqlshrc", "$CQLSHRCFILE" ]
#ENTRYPOINT [ "ls -la /cqlshrc" ]
