## Table of Contents

1. [What are web services?](#what-are-web-services)
2. [What is Amazon Web Services?](#what-is-amazon-web-services)
3. [Categories of AWS Services](#categories-of-aws-services)
4. [Some of the AWS Services in each category](#some-of-the-aws-services-in-each-category)
5. [Three ways to access AWS](#three-ways-to-access-aws)
6. [AWS Virtual Private Cloud (VPC)](#aws-virtual-private-cloud-vpc)
7. [AWS Route 53](#aws-route-53)
8. [AWS CloudFront](#aws-cloudfront)
9. [AWS Elastic Compute Cloud (EC2)](#aws-elastic-compute-cloud-ec2)
10. [AWS AMI](#aws-ami)
11. [AWS CloudWatch](#aws-cloudwatch)
12. [AWS Elastic Block Store (EBS)](#aws-elastic-block-store-ebs)
13. [AWS S3](#aws-s3)
14. [AWS Elastic File System (EFS)](#aws-elastic-file-system-efs)
15. [AWS Relational Database Service (RDS)](#aws-relational-database-service-rds)
16. [AWS DynamoDB](#aws-dynamodb)
17. [VPC Lab](#vpc-lab)
18. [EBS Lab](#ebs-lab)
19. [RDS Lab](#rds-lab)


### What are web services?
Web services are software systems designed to support interoperable machine-to-machine interaction over a network. They allow different applications to communicate with each other.

### What is Amazon Web Services?
Amazon Web Services (AWS) is a comprehensive cloud platform offering a wide range of global cloud-based products. This includes computing power, storage options, and databases, with pay-as-you-go pricing.

### Categories of AWS Services
AWS services are categorized into several groups, including:
- Compute
- Storage
- Databases
- Networking
- Security
- Analytics
- Developer Tools

### Some of the AWS Services in each category
Examples of AWS services by category:
- **Compute:** EC2, Lambda
- **Storage:** S3, EBS
- **Databases:** RDS, DynamoDB
- **Networking:** VPC, Route 53
- **Analytics:** Redshift, CloudWatch

### Three ways to access AWS
You can access AWS using:
1. AWS Management Console (web interface)
2. AWS Command Line Interface (CLI)
3. AWS SDKs (software development kits)

### AWS Virtual Private Cloud (VPC)
AWS VPC enables you to create a private network within the AWS cloud. It allows you to define your virtual environment, including IP address ranges, subnets, and route tables.

### AWS Route 53
AWS Route 53 is a scalable domain name system (DNS) web service that provides domain registration, DNS routing, and health checking of resources.

### AWS CloudFront
AWS CloudFront is a content delivery network (CDN) that delivers data, videos, applications, and APIs to users globally with low latency and high transfer speeds.

### AWS Elastic Compute Cloud (EC2)
AWS EC2 offers resizable compute capacity in the cloud, allowing users to run virtual servers on-demand.

### AWS AMI
AWS AMI (Amazon Machine Image) is a pre-configured template for creating virtual machines, containing the operating system and application software required for deployment.

### AWS CloudWatch
AWS CloudWatch is a monitoring service for AWS cloud resources and applications. It provides data and insights to help you monitor performance and optimize your applications.

### AWS Elastic Block Store (EBS)
AWS EBS is a block storage service for use with EC2 instances, providing persistent storage that can be attached to virtual machines.

### AWS S3
AWS S3 (Simple Storage Service) is an object storage service offering high durability, availability, and scalability for data storage and retrieval.

### AWS Elastic File System (EFS)
AWS EFS is a scalable file storage service for use with AWS cloud services and on-premises resources, allowing file storage to scale as needed.

### AWS Relational Database Service (RDS)
AWS RDS simplifies the setup, operation, and scaling of relational databases in the cloud, supporting various database engines.

### AWS DynamoDB
AWS DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability.   

### VPC Lab
#### Task 1: Create a VPC

> VPCs.
> ![](images/Screenshot%202024-08-22%20112336.png)



#### Task 2: Create Subnets
> Subnets.
> ![](images/Screenshot%202024-08-22%20112401.png)

> Route Tables.
> ![](images/Screenshot%202024-08-22%20112415.png)

> Internet Gateway.
> ![](images/Screenshot%202024-08-22%20112432.png)
#### Task 3: Create Security Groups


> Security Groups.
> ![](images/Screenshot%202024-08-22%20112457.png)

#### Task 4: Launch an EC2 Instance

> EC2 Instances.
> ![](images/Screenshot%202024-08-22%20113855.png)



> Open web browser via public IP.
> ![](images/Screenshot%202024-08-22%20111605.png)

> Open web browser via public DNS.
> ![](images/Screenshot%202024-08-22%20111544.png)