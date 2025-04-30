#SDA2020(Manal)
# Week 9 AWS Web Application Deployment
------------------------------------------------------
#Overview
In this project, I explain how to deploy a highly available website using AWS services such as S3, Auto Scaling Groups (ASG), and Application Load Balancer (ALB).
------------------------------------------------------
# Project Components:
1. S3: Used for hosting static assets (such as `index.html` and logo files).
2. Auto Scaling Group (ASG): Used for dynamically scaling NGINX web servers.
3. Application Load Balancer (ALB): Used for distributing incoming traffic to the web servers.
------------------------------------------------------
# Steps to Deploy:

1. S3 Setup:
   - Created an S3 bucket named `sda2020manal-clarusway-assets` and uploaded the `index.html` and logo files.
   - Enabled static website hosting for the bucket.
   - Configured public access using a bucket policy.

2. Auto Scaling Group:
   - Created an Auto Scaling Group with a minimum of 1, maximum of 3, and desired 2 NGINX instances.
   - Configured EC2 and ELB health checks.

3. Application Load Balancer:
   - Set up an ALB with an HTTP listener and health check.
   - Verified round-robin traffic distribution.
------------------------------------------------------
# Screenshots:
- s3-website-access.png
- s3-curl-response-200.png
- asg-min-max-desired.png
- asg-instance-screenshot.png
- alb-traffic-distribution.png
- alb-dns-screenshot.png
------------------------------------------------------
#Configuration Files:
- nginx-setup.sh: Script to install and configure NGINX on EC2 instances.
- s3-bucket-policy.json: Bucket policy to enable public read access.