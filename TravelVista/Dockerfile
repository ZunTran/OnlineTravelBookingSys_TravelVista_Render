FROM tomcat:11.0-jdk17

RUN rm -rf /usr/local/tomcat/webapps/*

EXPOSE 8080

COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

CMD sh -c 'sed -i "s/port=\"8080\"/port=\"${PORT:-8080}\"/" /usr/local/tomcat/conf/server.xml && catalina.sh run'
