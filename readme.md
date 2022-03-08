<img src = "readmeimages/google-cloud-logo-1.png" width = 500>

# **GCP CI/CD REPO**

This repository displays a CI/CD pipeline process for Google Cloud(GCP), using Cloud Build, Google Container Registry and Cloud run to continuously build and deploy a simple Java application.

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
