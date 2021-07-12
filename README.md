# aws-security-checklists

Note: IAM is used to provide permissions to all of the AWS Services, so it is not mentioned under each service.

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
* Enable encryption at rest
* Enable and Force access by SSL
* Enable auto minor version upgrade
* Rotate passwords periodically

## CloudWatch
* Use KMS Key for encrypting CloudWatch Log Groups.

## Kinesis
* Enable encryption at rest

## SQS
* Enable encryption at rest
* Assign appropriate SQL policy

## Systems Manager

## AWS Account
* Disable public S3 bucket access
* Enable MFA for root account
* Delete access key and secret for root account

## Lambda
* Encrypt environment variables
* Limit IAM role permissions

## Batch
* IAM based security
* AWS Batch uses ECS which in turn uses EC2 instances. Hence the security for ECS & EC2 instance apply.

## ECS / ECR / EKS

## AWS Backup
* Enable encryption for the resource that is being backed up. The AWS Backup uses the same KMS Key used for encrypting the resource.

## Dynamo DB
* Enable encryption at rest

## DMS

## CloudFront
* Use Lambda@Edge to add additional security headers
* Use appropriate SSL certificates
* Enable WAF
* Use regional restriction if applicable
* If integrating with S3, use origin identity
* Use latest TLS version
* Use custom error pages that do not reveal too much information
* Use signed cookies or signed urls if applicable

## Route 53
* Prevent unauthorized transfer to another registrar by enabling domain lock

## AWS Organization
* Use Service Control Policies/Organizational Units to control access in child AWS accounts.

## CloudFormation
* Enable drift detection
* Enable deletion protection if applicable
* Use IAM role for stack creation

## Config

## OpsWorks

## Service Catalog

## Athena

## IAM
* Use External ID if integrating with lots of third party AWS accounts

## Cognito

## Secrets Manager
* Utilize password rotation

## Certificate Manager

## KMS

## API Gateway
* Use MTLS for authentication
* Use API Key
* Set throttling in usage plans
* Use private API endpoint if invoking from within VPC

## Step Functions

## SNS

## PinPoint


