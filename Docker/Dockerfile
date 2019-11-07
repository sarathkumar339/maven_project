FROM centos:centos7
ENTRYPOINT ["/bin/bash"]
MAINTAINER sarathkuamr <sarathkumar339@gmail.com>
RUN yum install java-1.8.0-openjdk -y
RUN  yum install wget -y
RUN mkdir /opt/tomcat && cd /opt/tomcat/ && wget http://apachemirror.wuchna.com/tomcat/tomcat-8/v8.5.47/bin/apache-tomcat-8.5.47.tar.gz && tar -xvf apache-tomcat-8.5.47.tar.gz
ENV echo "export CATALINA_HOME=/opt/tomcat/apache-tomcat-8.5.47/" >>.bashrc
ENV echo "export PATH=$PATH:/opt/tomcat/apache-tomcat-8.5.47/bin" >>.bashrc
COPY warpro-1.0-SNAPSHOT.war /opt/tomcat/apache-tomcat-8.5.47/webapps
