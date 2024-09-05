#### **Overview**
This document outlines the infrastructure requirements for hosting a web application that consists of three main components:
1. **API Backend**: Hosted on AWS Elastic Beanstalk.
2. **Frontend**: Hosted on AWS S3.
3. **Database**: Managed using Amazon RDS (PostgreSQL).

#### **Infrastructure Components**

![Architecture](architecture%20diagram.png)

- **AWS Elastic Beanstalk**:
    - **Purpose**: Elastic Beanstalk is used to deploy and manage the API backend. It abstracts the infrastructure layer, allowing for quick deployment, scaling, monitoring, and management.
    - **Configuration**:
    - **Platform**: Node.js 14

- **AWS S3 (Simple Storage Service)**:
    - **Purpose**: S3 is used for hosting the static assets of the frontend, such as HTML, CSS, JavaScript, and media files.
    - **Configuration**:
    - **Bucket Name**: `myapp-frontend`
    - **Static Website Hosting**: Enable S3 bucket for static website hosting.
    - **Access Control**: Set up a bucket policy to allow public read access for website files.

- **Amazon RDS (Relational Database Service) for PostgreSQL**:
    - **Purpose**: RDS is used to manage the PostgreSQL database, which stores application data.
    - **Configuration**:
    - **DB Engine**: PostgreSQL
    - **VPC Security Group**: Configure inbound rules to allow access only from Elastic Beanstalk instances.