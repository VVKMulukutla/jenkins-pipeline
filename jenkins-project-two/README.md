# Jenkins Project Two

This project is a simple Java application that uses Jenkins for CI/CD.

## Jenkinsfile

The Jenkinsfile in this repository defines the Jenkins pipeline for this project.

### Stages

The pipeline consists of the following stages:

1. **Checkout scm**: This stage checks out the code from the repository.
2. **Build**: This stage builds the Java application.
3. **Test**: This stage runs the unit tests for the application.
4. **Deploy**: This stage deploys the application to a test environment.
5. **Disaster**: This stage deploys the application to a disaster recovery environment.
6. **Cleanup**: This stage cleans up the workspace.

### Prerequisites

The following prerequisites are required to run this Jenkinsfile:

- Java JDK 8 installed on the Jenkins server.
- Maven installed on the Jenkins server.
- Docker installed on the Jenkins server.
- AWS CLI installed on the Jenkins server.

### AWS Configuration

The AWS credentials are stored in Jenkins credentials store. These credentials are used to authenticate with AWS services.

### Docker Configuration

The following environment variables are used to configure Docker in the Jenkinsfile:

- **AWS_ACCESS_KEY_ID**: The AWS access key ID.
- **AWS_SECRET_ACCESS_KEY**: The AWS secret access key.
- **AWS_DEFAULT_REGION**: The AWS region.
- **ECR_REPO**: The Amazon ECR repository URI.
- **ECR_IMAGE**: The Docker image name.
- **ECR_TAG**: The Docker image tag.

### Jenkins Configuration

The following environment variables are used to configure Jenkins in the Jenkinsfile:

- **JENKINS_USER**: The Jenkins user.
- **JENKINS_PASS**: The Jenkins password.
- **JENKINS_URL**: The Jenkins URL.

### Deployment

The application is deployed to an Amazon ECS cluster using the AWS CLI. The ECS task definition and service are created in the AWS console.

## Usage

To run the Jenkins pipeline, trigger the Jenkins job.

