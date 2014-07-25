StrutsWebappGradle
==================

create build.gradle and add the required plugins
    java
    war
    eclipse-wtp
    jetty

mkdir -p src/main/java
mkdir -p src/main/test
mkdir -p src/main/webapp
mkdir -p src/main/resources


Once the structure as defined above is created run below command to generate eclipse related files
gradle eclipse

Each and every time when a dependencies is added to build.gradle, 
the eclipse might give compilation error as it will not be able to refer the dependcies jar directly 
(just by including in build file). you have to run
gradle eclipse
and then refresh project inside eclipse so compilation errors go away inside eclipse


to start the server and deploy war use the task
gradle jettyRunWar

If you want to debug this project, have this export and restart the server
export GRADLE_OPTS="-Xdebug -Xrunjdwp:transport=dt_socket,address=9999,server=y,suspend=n"

Ref::
http://www.javacodegeeks.com/2013/04/simple-gradle-web-application.html
