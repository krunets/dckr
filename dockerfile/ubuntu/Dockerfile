FROM ubuntu
  
RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN apt -y update && apt -y upgrade && apt -y install curl
RUN curl --version
RUN curl -O https://downloads.apache.org/tomcat/tomcat-8/v8.5.66/bin/apache-tomcat-8.5.66.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-8.5.66/* /opt/tomcat/.
RUN apt -y install openjdk-8-jdk

RUN java -version

WORKDIR /opt/tomcat/webapps
#RUN curl -O -L https://github.com/AKSarav/SampleWebApp/raw/master/dist/SampleWebApp.war

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]