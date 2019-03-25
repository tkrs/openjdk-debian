FROM debian:stretch-slim

ENV JAVA_HOME /usr/lib/jvm/openjdk
ENV PATH $JAVA_HOME/bin:$PATH

RUN mkdir -p $JAVA_HOME; \
    apt-get update && \
    apt-get install -y --no-install-recommends curl ca-certificates && \
    curl -sS -o - https://download.java.net/java/early_access/jdk13/13/GPL/openjdk-13-ea+13_linux-x64_bin.tar.gz | \
    tar -z --extract --file - --directory $JAVA_HOME --strip-components 1


CMD java
