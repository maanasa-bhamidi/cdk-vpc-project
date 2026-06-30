# AWS CDK VPC Project

## What this project does
Builds a secure AWS network infrastructure using Python and AWS CDK.
Deploys a VPC with public and private subnets, a Security Group controlling
HTTP and SSH traffic, and an IAM Role giving EC2 instances read-only S3 access.
Everything deploys with a single command - no clicking in the AWS console.

## AWS Services Used
- Amazon VPC - private network with public and private subnets
- EC2 Security Group - allows port 80 (HTTP) and port 22 (SSH)
- AWS IAM - Role allowing EC2 to read from S3 without stored credentials
- AWS CDK - infrastructure as code using Python

## How to Deploy
git clone https://github.com/maanasa-bhamidi/cdk-vpc-project
cd cdk-vpc-project
pip install -r requirements.txt
cdk bootstrap
cdk deploy

## How to Destroy
## What I Learned
- How to build cloud infrastructure using Python code instead of clicking in AWS console
- How Security Groups control traffic using ingress and egress rules
- How IAM Roles give AWS services permissions without storing credentials
- The difference between cdk synth, cdk diff, cdk deploy and cdk destroy

## Author
Maanasa Bhamidi
GitHub: https://github.com/maanasa-bhamidi
