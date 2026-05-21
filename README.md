# AWS S3 Static Website Lab

## Overview
This lab demonstrates how to host a static website on Amazon S3 using the AWS CLI and Management Console.

## Topics Covered
- Create an Amazon S3 bucket using AWS CLI
- Create an IAM user with full S3 access
- Upload website files to Amazon S3
- Enable static website hosting
- Adjust S3 bucket permissions
- Create a batch file for automated website updates

## Tools & Services Used
- Amazon S3
- AWS IAM
- AWS CLI
- Amazon EC2 (Session Manager)

## Steps Performed
1. Connected to EC2 instance using AWS Systems Manager
2. Configured AWS CLI with credentials
3. Created an S3 bucket using `aws s3api create-bucket`
4. Created IAM user `awsS3user` with full S3 access
5. Uploaded static website files using `aws s3 cp`
6. Enabled static website hosting
7. Created a batch file for repeatable deployments
8. Used `aws s3 sync` for efficient file updates

## Key Commands Used
\```bash
aws configure
aws s3api create-bucket --bucket <bucket-name> --region <region>
aws iam create-user --user-name awsS3user
aws s3 website s3://<bucket-name>
aws s3 cp <local-path> s3://<bucket-name>
aws s3 sync <local-path> s3://<bucket-name>
\```

## Conclusion
Successfully hosted a static website on Amazon S3 with secure IAM permissions and automated deployment using AWS CLI.
