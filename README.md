# Employee Form Web Application

## Project Overview
This is a simple web application built using Java, Maven, and Jenkins. The application provides an employee details form and is packaged as a WAR file for deployment to an Apache Tomcat server.

## Project Structure
- **Jenkinsfile**: Defines the CI/CD pipeline, including repository cloning, building with Maven, and deployment to Tomcat.
- **pom.xml**: The Maven configuration file specifying dependencies and build plugins.
- **index.html**: The main webpage containing a form for employee details.
- **web.xml**: Web descriptor file for the Java web application.

## Technologies Used
- Java
- Maven
- Jenkins
- Tomcat
- HTML

## Prerequisites
- Install Java (JDK 8 or later)
- Install Apache Maven (3.8.7 recommended)
- Install Apache Tomcat (8 or later)
- Install Jenkins with required plugins (Git, Maven Integration, Deploy to Container)

## Installation & Setup
1. **Clone the Repository:**
   ```sh
   git clone https://github.com/mmbabu1988/build-deploy.git
   ```
2. **Navigate to the project directory:**
   ```sh
   cd build-deploy
   ```
3. **Build the project using Maven:**
   ```sh
   mvn clean install
   ```
4. **Deploy the WAR file to Tomcat:**
   - Copy the generated WAR file from `target/web-application-war-file.war` to Tomcat's `webapps` directory.
   - Start Tomcat and access the application at `http://localhost:8080/web-application-war-file`.

## CI/CD Pipeline (Jenkins)
This project uses Jenkins for continuous integration and deployment.
- **Triggers**: The pipeline is set to run every 10 minutes via a cron job.
- **Stages**:
  1. Clone repository from GitHub.
  2. Build the project using Maven.
  3. Deploy the generated WAR file to the Tomcat server.

## Deployment
Jenkins automatically deploys the application to the Tomcat server at:
```
http://54.224.167.178:9090/
```

## Troubleshooting
- If the build fails, ensure that Maven is correctly installed and configured.
- If Tomcat deployment fails, check the credentials in Jenkins.
- If the application does not load, verify that Tomcat is running on the correct port.



