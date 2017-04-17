# version: 0.0.1
FROM centos:latest

MAINTAINER Gollum 'jianqiao.ms@foxmail.com'

RUN yum install -y wget

RUN wget https://packages.jianqiao.tk/jre-7u80-linux-x64.tar.gz && tar zxvf jre-7u80-linux-x64.tar.gz && \
    rm -rf jre-1.7.0_80 && rm -rf /opt/jre-1.7.0_80 && \
    mv jre-1.7.0_80 /opt/ && ln -s /opt/jre-1.7.0 /usr/local/jre && \
    echo 'JAVA_HOME=/usr/local/jdk' > /etc/profile.d/jdk.sh && \
    echo 'CLASSPATH=$JAVA_HOME/lib' >> /etc/profile.d/jdk.sh && \
    echo 'pathmunge $JAVA_HOME/bin' >> /etc/profile.d/jdk.sh

CMD ["/bin/bash"]
