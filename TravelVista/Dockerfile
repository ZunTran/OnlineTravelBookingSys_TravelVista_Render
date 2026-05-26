FROM tomcat:11.0-jdk17

RUN rm -rf /usr/local/tomcat/webapps/*

ENV JAVA_OPTS="-Djava.security.egd=file:/dev/./urandom -Xms128m -Xmx384m -Dtomcat.util.http.parser.HttpParser.requestTargetAllow='|{}'"

COPY target/*.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080

CMD ["catalina.sh", "run"]
