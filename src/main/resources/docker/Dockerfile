FROM centos:7

RUN yum -y install wget
#RUN wget --no-cookies --no-check-certificate --header "Cookie: oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u77-b03/jre-8u77-linux-x64.rpm" -O /tmp/jdk-8-linux-x64.rpm
RUN wget --no-cookies --no-check-certificate --header "Cookie: oraclelicense=accept-securebackup-cookie" "https://download.oracle.com/otn-pub/java/jdk/8u192-b12/750e1c8617c5452694857ad95c3ee230/jdk-8u192-linux-x64.rpm" -O /tmp/jdk-8-linux-x64.rpm
RUN yum -y install /tmp/jdk-8-linux-x64.rpm
ENV JAVA_HOME /usr/java/latest


RUN mkdir /opt/helloworld
COPY helloworld.jar /opt/helloworld/
ENTRYPOINT ["java", "-jar", "/opt/helloworld/helloworld.jar"]
