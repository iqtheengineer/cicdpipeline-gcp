<img src = "readmeimages/google-cloud-logo-1.png" width = 500>

# **GCP CI/CD REPO**

This repository displays a CI/CD pipeline process for Google Cloud(GCP), using Terraform, Cloud Build, Google Container Registry and Cloud run to build a simple java application, store the docker image in Google Container Registry and deploy it to Google Cloud Run.

The diagram was created using Google Cloud's new diagram tool. You can learn more about it here: https://googlecloudcheatsheet.withgoogle.com/architecture

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
- This is a terraform file which creates a trigger on Google Cloud Build on the supplied parameters
