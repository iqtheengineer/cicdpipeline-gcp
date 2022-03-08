<img src = "readmepics/tomcat.jpg" width = 300>

# **Tomcat**
**Tomcat 8 Docker Repository**

This repository contains files to run a sample application on Tomcat 8 and demonstrates a CI/CD process in action.

# **The Docker file**
- Builds the tomcat 8.5 instance from scratch
- Clones the source code of a sample web application
- Builds the application using maven
- Copies the built war file to the webapps directory as ROOT.war
- Runs catalina.sh as entrypoint script

# **The cloudbuild.yaml file**
- Contains configuration to use the Google Cloud Build service which
- Builds the docker image in Google Cloud Platform
- Pushes the container image in to Google Cloud Registry
- Deploys the image to Google Cloud Run

# **The main.tf file**
- Is a terraform file which creates a trigger on Google Cloud Build on the supplied parameters
