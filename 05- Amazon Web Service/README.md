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
17. [Labs](#labs)
    - [VPC Lab](#vpc-lab)
    - [EBS Lab](#ebs-lab)
    - [RDS Lab](#rds-lab)
    - [Auto Scaling Group and ELB Lab](#auto-scaling-group-and-elb-lab)


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

### Labs

### VPC Lab
#### Task 1: Create a VPC

> VPCs.
> ![](images/vpc-lab/Screenshot%202024-08-22%20112336.png)



#### Task 2: Create Subnets
> Subnets.
> ![](images/vpc-lab/Screenshot%202024-08-22%20112401.png)

> Route Tables.
> ![](images/vpc-lab/Screenshot%202024-08-22%20112415.png)

> Internet Gateway.
> ![](images/vpc-lab/Screenshot%202024-08-22%20112432.png)
#### Task 3: Create Security Groups


> Security Groups.
> ![](images/vpc-lab/Screenshot%202024-08-22%20112457.png)

#### Task 4: Launch an EC2 Instance

> EC2 Instances.
> ![](images/vpc-lab/Screenshot%202024-08-22%20113855.png)



> Open web browser via public IP.
> ![](images/vpc-lab/Screenshot%202024-08-22%20111605.png)

> Open web browser via public DNS.
> ![](images/vpc-lab/Screenshot%202024-08-22%20111544.png)


### EBS Lab
#### Task 1: Create an EBS Volume

> EBS Volumes.
> ![](images/ebs-lab/Screenshot%202024-08-23%20095129.png)

#### Task 2: Attach EBS Volume to EC2 Instance

> Attached EBS Volume.
> ![](images/ebs-lab/Screenshot%202024-08-23%20095228.png)
> ![](images/ebs-lab/Screenshot%202024-08-23%20095402.png)


#### Task 3: Connect to EC2 Instance Using SSH

> SSH Connection.
> ![](images/ebs-lab/Screenshot%202024-08-23%20100809.png)


#### Task 4: Create and Configure File System


> File System.
> ![](images/ebs-lab/Screenshot%202024-08-23%20100830.png)
> ![](images/ebs-lab/Screenshot%202024-08-23%20101516.png)


#### Task 5: Create an EBS Snapshot

> EBS Snapshot.
> ![](images/ebs-lab/Screenshot%202024-08-23%20102648.png)

> Delete file.txt.
> ![](images/ebs-lab/Screenshot%202024-08-23%20102625.png)


#### Task 6: Restore EBS Volume from Snapshot

> Restored EBS Volume.
> ![](images/ebs-lab/Screenshot%202024-08-23%20102935.png)
> ![](images/ebs-lab/Screenshot%202024-08-23%20103107.png)



### RDS Lab
#### Task 1: Create a Security Group for RDS

> RDS Security Group.
> ![](images/rds-lab/Screenshot%202024-08-24%20142500.png)


#### Task 2: Create a DB Subnet Group

> DB Subnet Group.
> ![](images/rds-lab/Screenshot%202024-08-24%20142850.png)


#### Task 3: Create an Amazon RDS Instance

> RDS Instance.
> ![](images/rds-lab/Screenshot%202024-08-24%20144356.png)

#### Task 4: Connect to RDS Instance from EC2 Instance

> Connect to RDS.
> ![](images/rds-lab/Screenshot%202024-08-24%20151334.png)


### Auto Scaling Group and ELB Lab
#### Task 1: Create an AMI for Auto Scaling

> AMI for Auto Scaling.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20144604.png)


#### Task 2: Create a Load Balancer

> Load Balancer.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20145104.png)



#### Task 3: Create an Auto Scaling Group

> Auto Scaling Group.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20150644.png)



#### Task 4: Verify Load Balancer is Working

> Load Balancer Working.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20151534.png)

> Target Group.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20152031.png)

> Load Balancer DNS.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20152226.png)
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20152242.png)



#### Task 5: Test Auto Scaling

> Auto Scaling Test using CloudWatch.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20153110.png)


#### Task 6: Terminating Instances

> Terminating Instances.
> ![](images/auto-scaling-and-elb-lab/Screenshot%202024-08-25%20153204.png)