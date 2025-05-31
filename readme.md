Automate Deploy a registration web page from sourcecode management to apache tomcatserver using jenkins
This repo consist a simple Registrstion app with maven pom.xml 

# To build tomcat server docker image run cmd :
               
               docker build -t tomcat-server .

# to run the image run cmd :
                
               docker run -d -p 8080:8080 --name mytomcat tomcat-server

# It runs on http://localhost:8080
# copy the tomcat server url to use in jenkins