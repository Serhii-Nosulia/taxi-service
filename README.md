# Taxi-Service
___
This is a simple web application that represents the work of a taxi service.
It implements authentication and registration mechanisms. Supports interaction with RDBMS

## Features
___

- registration like a driver;
- authentication like a driver;
- create/delete/update a driver;
- create/delete/update a manufacturer;
- create/delete/update a car;
- display a list of all drivers;
- display a list of all manufacturers;
- display a list of all cars;
- display a list of cars that the current driver has;

## Project structure
___

- ``src/main``- main project directory;
    - ``src/main/java`` - Java class files;
        - ``src/main/taxi`` - main Java package;
            - ``src/main/java/taxi/controller`` - Java package that contains Java servlets;
            - ``src/main/java/taxi/dao`` - Java package that contains DAO classes;
            - ``src/main/java/taxi/exception`` - Java package that contains custom exceptions classes;
            - ``src/main/java/taxi/lib`` - Java package that contains Injector class and his annotations;
            - ``src/main/java/taxi/model`` - Java package that contains model classes: Car, Driver, and Manufacturer;
            - ``src/main/java/taxi/service`` - Java package that contains different service classes;
            - ``src/main/java/taxi/util`` - Java package that contains ConnectionUtil class;
            - ``src/main/java/taxi/web/filter`` - Java package that contains Java filter;
    - ``src/mein/resources`` - directory that contains SQL file for DB initialization;
    - ``src/main/webapp`` - directory that contains webapp files;
    - ``src/main/webapp/WEB-INF`` - directory that contains main webapp files;
        - ``src/main/webapp/WEB-INF/web.xml`` - webapp configuration file;
        - ``src/main/webapp/WEB-INF/views`` - directory that contains JSP pages;
- ``checkstyle.xml`` - configuration file for checkstyle maven plugin;
- ``pom.xml`` - Maven configuration file;
- ``README.md`` - readme file;

## Usage technologies:
___

- [JAVA](https://en.wikipedia.org/wiki/Java_(software_platform))
- [Jakarta Servlet](https://en.wikipedia.org/wiki/Jakarta_Servlet)
- [Jakarta Server Pages](https://en.wikipedia.org/wiki/Jakarta_Server_Pages)
- [Java Database Connectivity](https://en.wikipedia.org/wiki/Java_Database_Connectivity)
- [HTML](https://en.wikipedia.org/wiki/HTML), [CSS](https://en.wikipedia.org/wiki/CSS)

## Startup Guide
___

If you decide to run this project, you need to get at least java 17 and MySQL.
A file with SQL code (a package named "resources" at the same level as the "java" package)
can be compiled in the MySQL environment. When your database is ready to use,
you need to change some fields in ConnectionUtil.class:

**Tomcat configuration:**
To add the tomcat configuration you need to choose: Run -> Edit Configurations ->
click the plus in the upper left corner -> find the Tomcat server -> local -> configure...
(in the right window that appears) -> paste the path , where your tomcat is installed -> OK ->
Fix (bottom right corner) -> select "war exploded artifact" -> deployment (top panel) ->
change application context to "/".