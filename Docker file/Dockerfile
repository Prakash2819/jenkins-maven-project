FROM tomcat:9.0

# ✅ Restore default webapps including manager and host-manager
RUN cp -R /usr/local/tomcat/webapps.dist/* /usr/local/tomcat/webapps/

# ✅ Deploy your WAR file (optional)
COPY ./*.war /usr/local/tomcat/webapps/

# ✅ Set up tomcat-users.xml with required roles
COPY tomcat-users.xml /usr/local/tomcat/conf/

# ✅ Copy custom context.xmls to allow remote access
COPY manager-context.xml /usr/local/tomcat/webapps/manager/META-INF/context.xml
COPY host-manager-context.xml /usr/local/tomcat/webapps/host-manager/META-INF/context.xml

EXPOSE 8080
CMD ["catalina.sh", "run"]



