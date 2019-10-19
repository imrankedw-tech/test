## Introduction to AWS Services

#### AWS Introduction, Commonly used services & high level Security concepts 
- What is ? 
- Timeline 
	
	Below are one of most important services launched yearwise. 
        
	2008 Amazon Elastic Block Storage
        
	2009 AWS Management Console
        
	2010 Amazon SNS
        
	2010 AWS Identity and Access Management
        
	2010 Amazon Route 53
        
	2011 AWS Elastic Beanstalk
        
	2011 AWS CloudFormation
        
	2012 Dynamo DB

- Regions
- AZ
- EndPoint
- ARN		

## Amazon EC2 & S3

#### Introduction to EC2 & S3
- Instances
- AMI's
- Instance Sores
- EBS
- Snapshots
*Security Concepts recap*
- Private IP 
- Public IP / Elastic IP 
- Users, Roles & Profiles configuraitons
- Connecting to EC2
- EC2 Service Limits
- Best Practises 
		
		Security Best Practices:
		Use IAM to control access to EC2 instances
		Use IAM users/roles and assign security credentails to restrict access to instances 
		Use Security Group for restricting access to trusted host, network (IP Address ranges) & port numbers
		Use least privilege rule: meaning use permissions which are only required
		Use periodic review of security groups
		Disable password based logins for instances which can be launched from AMI's.
		
	Storage:
	
		Plan for data persistance, backup & recovery
		Saperate EBS volumes for OS and data (Ensure volume with your data is persisted after instance termination)
		Use instance store for temperory data.
		
	Resource Management:
	
		Use instance metadata or tags to identify resources.
		Review currently allocated resources and threshold / soft limit in your region, early request limit increase if needed
		
	Backup & Recovery:
	
		Periodic backup of EBS Volume and creating AMI from existing instance.
		Plan replication strategy for critical data needs
		Monitor events (CPU / memory / diskspace), using cloud watch notifications
		Prepare for failover by using elastic ip (For automated solution we can use EC2 autoscaling)
		Periodically test recovering of instance or EBS Volumes from existing backups
[S3 Notes](s3.txt)
#### Introduction
#### Serverless
#### Bucket Operations
#### Bucket Security config & other configs 
#### Metadata, Storage Class, Versioning, LifeCycle Management & Cors Config.
#### Object Operations (upload via. CLI & Python boto3 API) 
#### Limitations
#### S3 and its integration with other services (Lambda + SQS)


## Amazon Redshift 
#### Introduction & High level Architecture
#### Creating a Cluster  & Connecting to Database
#### DDL, DML, DCL Operations
#### Table design techniques
#### Loading data 
#### Managing Cluster
#### Redshift Spectrum
#### Redshift + Python + UDF's
