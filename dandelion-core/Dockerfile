# Dandelion-Core 0.10.0
FROM centos:6.4
MAINTAINER Thibault Duchateau <thibault.duchateau@gmail.com>

# Install utilities
RUN yum install -y vim git sudo tar zip bzip2 wget

# Install JDK 1.6
RUN yum install -y java-1.6.0-openjdk && \
    echo "export JAVA_HOME=/usr/lib/jvm/java-1.6.0-openjdk.x86_64" >> ~/.bashrc

# Install Maven
RUN wget http://repos.fedorapeople.org/repos/dchen/apache-maven/epel-apache-maven.repo -O /etc/yum.repos.d/epel-apache-maven.repo && \
    yum install -y apache-maven && \
    ln -s /usr/share/apache-maven/bin/mvn /usr/local/bin/mvn

# Install PhantomJS and related utilities
RUN yum install -y fontconfig freetype && \
    cd /tmp && \
    wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-1.9.7-linux-x86_64.tar.bz2 && \
    tar xvf phantomjs-1.9.7-linux-x86_64.tar.bz2 && \
    cp /tmp/phantomjs-1.9.7-linux-x86_64/bin/phantomjs /usr/local/bin && \
    rm -rf /tmp/phantomjs-1.9.7-linux-x86_64 /tmp/phantomjs-1.9.7-linux-x86_64.tar.bz2

# Download project sources
RUN mkdir /dandelion && \
    cd /dandelion && \ 
    git clone https://github.com/dandelion/dandelion.git

# Build
RUN cd /dandelion/dandelion && \
    mvn clean package