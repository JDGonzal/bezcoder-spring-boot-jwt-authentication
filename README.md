# Spring Boot Token based Authentication with Spring Security & JWT
https://www.bezkoder.com/spring-boot-jwt-authentication/

## Steps to start for all
1. Install Postman
   [Postman Download](https://www.postman.com/downloads/)
2. Install MySQL 5.6.x
   [MySQL Download 5.6.26](https://downloads.mysql.com/archives/community/)
3. Install IntelliJ IDEA
   [IntelliJ IDEA](https://www.jetbrains.com/es-es/idea/download/#section=windows)
4. Press into Intellij Editor, [Ctrl]+[Alt]+[S], and select Plugins.<br />
   Check for those in your list:
   * Hibernate Inspections (Marcelo Glasberg)
   * Spring & Java Tools(Beeant)
   * JPA Support (carter-ya)
   * Maven (bundled)
   * Eclipse Interoperability (bundled)
5. Create a DB called "bezkoder" and
   You could create the DB using a script
  ```sql
    CREATE DATABASE IF NOT EXISTS bezkoder;

    USE bezkoder;
  ```

## Steps to work the API
1. Create a Structure like this: <br />
   ![alt text](https://www.bezkoder.com/wp-content/uploads/2019/10/spring-boot-authentication-spring-security-project-structure.png)
2. Setting up the "pom.xml" file adding some dependencies
3. Make some corrections on "application.properties" file
4. But to keep some secrets use the "env.properties", called after with:
   ```java
   spring.config.import=optional:file:env.properties
   ```
5. Example of "application.properties" file
   ```ini
   #MYSQL CONNECTION
   MYSQL_HOST=________
   MYSQL_USER=________
   MYSQL_PASS=________
   MYSQL_D_B_=________
   MYSQL_PORT=________

   #AUTH KEY
   AUTH_SECRET_KEY=_______
   ```
6. Until this step, the application, can run, because it can connect to MySQL DB.

## To run at end you can use two ways
1. At the end, run this command to up the API, to check in Postman 'http://localhost:8080/api/',
  ```bash
  mvn spring-boot:run
  ```
2. or Using the Editor in "Run" option the "SpringBootSecurityJwtApplication"
