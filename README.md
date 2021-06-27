# aws-security-checklists


## S3
* Enable [Encryption at Rest](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucket-encryption.html)
* Enable [Encryption in Transit](https://aws.amazon.com/premiumsupport/knowledge-center/s3-bucket-policy-for-config-rule/)
* Block [Public Access at AWS Account level](https://aws.amazon.com/s3/features/block-public-access/)
* Block [Public Access at Bucket level](https://aws.amazon.com/s3/features/block-public-access/)
* Use [VPC endpoint for S3](https://docs.aws.amazon.com/vpc/latest/privatelink/vpc-endpoints-s3.html)
* Use [GuardDuty for threat detection](https://aws.amazon.com/blogs/aws/new-using-amazon-guardduty-to-protect-your-s3-buckets/)
* Use [Macie to detect sensitive data](https://aws.amazon.com/blogs/aws/new-enhanced-amazon-macie-now-available/)
* Configure [MFA Delete](https://docs.amazonaws.cn/en_us/AmazonS3/latest/userguide/MultiFactorAuthenticationDelete.html) for applicable buckets.
* Use [S3 Object Lock](https://docs.amazonaws.cn/en_us/AmazonS3/latest/userguide/object-lock.html) to meet regulatory requirements
* Set appropriate [bucket policies](https://docs.aws.amazon.com/AmazonS3/latest/userguide/example-bucket-policies.html)

## EC2, EBS, EFS
* Enable Encryption at Rest
* Allow specific and limited IP addresses and ports in security group for both inbound and outbound
* Create EC2 in private subnet if applicable.
* Install recommended security tools (anti virus, threat detection, etc.,)
* Use secure AMI from known provider
* Use only required permissions for the IAM role attached to EC2 instance.
* Use end-to-end encryption in transit.

## VPC
* Use Gateway endpoints for S3 and Dynamo DB
* Use VPC endpoints for other AWS services where applicable
* Enable VPC Flow Logs
* Remove the default inbound and outbound entries in default security group of the VPC
* Set VPC Endpoint policy

## RDS
* Restrict RDS access to specific IP addresses
* Place RDS in private subnet
* Disable Public access to instance and snapshots
* Enable Encryption at Rest
* Enable and Force access by SSL
* Enable auto minor version upgrade
* Rotate passwords periodically

## CloudWatch

## Kinesis

## SQS

## Systems Manager

## AWS Account

## Lambda

## Batch

## ECS / ECR / EKS

## AWS Backup

## Dynamo DB

## DMS

## CloudFront

## Route 53

## CodeTools

## AWS Organization
* SCP
* 

## CloudFormation

## Config

## OpsWorks

## Service Catalog

## Athena

## IAM
* External ID

## Cognito

## Secrets Manager

## Certificate Manager

## KMS

## API Gateway

## Step Functions

## SNS

## PinPoint

## 
