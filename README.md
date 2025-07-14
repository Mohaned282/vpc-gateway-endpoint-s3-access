# Private S3 Access via VPC Gateway Endpoint

## Overview
This project demonstrates how to securely access Amazon S3 from a private EC2 instance **without internet access**, using a VPC Gateway Endpoint. All steps were performed using the AWS Console.

## Architecture
- **VPC CIDR**: 10.0.0.0/16
- **Public Subnet**: 10.0.1.0/24 (contains Ubuntu EC2 as bastion host)
- **Private Subnet**: 10.0.2.0/24 (contains Amazon Linux AMI EC2 instance)
- **Endpoint Type**: Gateway Endpoint for S3

## Key Steps
- Created a VPC with public and private subnets.
- Launched a **public Ubuntu EC2 instance** to act as a **bastion host**.
- Launched a **private Amazon Linux AMI EC2 instance** with no internet access.
- Configured **SSH access** from public to private EC2.
- Added a **VPC Gateway Endpoint** for S3 to the route table of the private subnet.
- Verified private S3 access using: `aws s3 ls` from the private EC2 instance.

## Key Skills Demonstrated
- **VPC Gateway Endpoints**: Configuring private, secure access to AWS services like S3 without using NAT or IGW.
- **Amazon EC2**: Deploying and managing Linux-based compute instances in public and private subnets.
- **Private Subnet Architecture**: Isolating compute resources with no direct internet connectivity.
- **AWS Security Groups & SSH Access**: Controlling secure access to EC2 instances using a bastion host.
- **Amazon S3 Access Control**: Verifying and restricting S3 access using endpoint policies and IAM.

## Screenshots
Screenshots of the full implementation are included in this repository.

## Author
Mohaned Mohamed  
Glasgow, United Kingdom  
m.gorashi282@gmail.com | +447417414418  
[LinkedIn Profile](https://www.linkedin.com/in/mohaned-mohamed-64674a45/) | [GitHub Profile](https://github.com/Mohaned282)