#
# dandelion/base-sample
#
FROM tomcat:7
MAINTAINER Thibault Duchateau <thibault.duchateau@gmail.com>

ENV MAVEN_HOME /usr/local/apache-maven-3.2.5
ENV PATH $MAVEN_HOME/bin:$PATH

# Install Maven
RUN wget -q -nv http://apache.crihan.fr/dist/maven/maven-3/3.2.5/binaries/apache-maven-3.2.5-bin.zip -P /usr/local && \
    cd /usr/local && \
    unzip apache-maven-3.2.5-bin.zip && \
    rm -f apache-maven-3.2.5-bin.zip &&
