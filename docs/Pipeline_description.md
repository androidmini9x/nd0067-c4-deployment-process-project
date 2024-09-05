### **Pipeline_description.md**

#### **Overview**
This document explains the different steps involved in the CI/CD pipeline for deploying the web application, which consists of a frontend and an API backend. The pipeline is divided into three main stages: **Build**, **Hold**, and **Deploy**.

#### **Pipeline Stages**

![Pipeline Stages](Pipeline%20Diagram.png)

1. **Build Stage**
   - **Purpose**: Prepare the environment, install dependencies, and build both the frontend and API components of the application.
   - **Steps**:
     1. **Spin up environment**: Initialize the build environment, including provisioning necessary compute resources.
     2. **Preparing environment variables**: Set up environment variables required for the build process (e.g., API keys, build secrets).
     3. **Install Node.js 14.15**: Install the specified Node.js version (14.15) for building the frontend and backend.
     4. **Checkout code**: Pull the latest version of the code from the source repository (e.g., GitHub, Bitbucket).
     5. **Install Front-End Dependencies**: Run package manager commands (e.g., `npm install` or `yarn install`) to install frontend dependencies.
     6. **Install API Dependencies**: Run the appropriate package manager command to install API backend dependencies.
     7. **Front-End Lint**: Lint the frontend codebase using configured linting tools (e.g., ESLint) to ensure code quality and style adherence.
     8. **Front-End Build**: Build the frontend application (e.g., `npm run build`) to generate static files for deployment.
     9. **API Build**: Build the API backend using the appropriate build tools or scripts (e.g., `mvn package` for Java, `npm run build` for Node.js).

2. **Hold Stage**
   - **Purpose**: Introduce a manual approval step to verify the build artifacts before deploying them to production.
   - **Steps**:
     1. **Manually Approved**: The pipeline is paused until a designated user manually approves the deployment. This step is a gatekeeper to prevent automatic deployment and allows for final validation, testing, or any required checks.

3. **Deploy Stage**
   - **Purpose**: Deploy the built application (frontend and API) to the AWS environment.
   - **Steps**:
     1. **Spin up environment**: Initialize the deployment environment, setting up any required AWS resources.
     2. **Preparing environment variables**: Prepare the deployment environment variables needed for the application to run (e.g., API keys, database credentials).
     3. **Install Node.js 14.15**: Install Node.js version 14.15 to ensure compatibility with the deployment scripts.
     4. **Setting Up Elastic Beanstalk CLI**: Install and configure the Elastic Beanstalk CLI to interact with AWS Elastic Beanstalk.
     5. **Install AWS CLI - latest**: Install the latest version of the AWS CLI to manage AWS services and resources during deployment.
     6. **Configure AWS Access Key ID**: Set up AWS credentials (Access Key ID and Secret Access Key) to authenticate and authorize deployment actions.
     7. **Checkout code**: Pull the latest code version from the repository for deployment.
     8. **Deploy App FRONT_END**: Deploy the built frontend application to AWS S3 or CloudFront (if using CDN).
     9. **Deploy App**: Deploy the built API backend to AWS Elastic Beanstalk using the Elastic Beanstalk CLI.