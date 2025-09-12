# jenkins-docker-project/README.md

# Jenkins Docker Project

This project sets up a Jenkins environment using Docker to build a static website. It includes a Jenkins pipeline defined in the `Jenkinsfile`, a Docker Compose configuration in `docker-compose.yml`, and a custom Docker image defined in `Dockerfile`.

## Project Structure

- **Jenkinsfile**: Defines the Jenkins pipeline for building the static website. It includes stages for checking out the code, building the website, publishing the HTML using the HTML Publisher plugin, and archiving build artifacts.
  
- **docker-compose.yml**: Configuration file for running Jenkins with Docker Compose. It specifies the necessary ports, volumes, and the Jenkins image to be used.
  
- **Dockerfile**: Custom Docker image for Jenkins, which may include instructions for installing necessary dependencies and plugins required for building the static website.
  
- **README.md**: Documentation for the project, including setup instructions and usage guidelines.

## Setup Instructions

1. **Clone the Repository**: 
   ```bash
   git clone <repository-url>
   cd jenkins-docker-project
   ```

2. **Start Jenkins**:
   Run the following command to start Jenkins using Docker Compose:
   ```bash
   docker-compose up -d
   ```

3. **Access Jenkins**:
   Open your web browser and go to `http://localhost:8080`. Follow the instructions to unlock Jenkins.

4. **Create a New Pipeline**:
   - In Jenkins, create a new item and select "Pipeline".
   - Configure the pipeline to use the `Jenkinsfile` in your repository.

5. **Build the Project**:
   Trigger the build in Jenkins to start the pipeline, which will check out the code, build the static website, publish the HTML, and archive the artifacts.

## Usage Guidelines

- Ensure that Docker and Docker Compose are installed on your machine.
- Modify the `Dockerfile` as needed to include any additional dependencies required for your static website.
- Customize the `Jenkinsfile` to suit your specific build and deployment needs.

## Additional Information

For more details on Jenkins and Docker, refer to the official documentation:
- [Jenkins Documentation](https://www.jenkins.io/doc/)
- [Docker Documentation](https://docs.docker.com/)