# SDA2020(Manal)
# Week 9 AWS Web Application Deployment
------------------------------------------------------
# Overview
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

-s3-website-access.png: Shows the access to the static website hosted on Amazon S3.

-s3-curl-response-200.png: Displays the output of a curl command showing a 200 OK response from the S3 bucket, confirming the successful setup of the static website.

-asg-min-max-desired.png: Shows the configuration of the Auto Scaling Group, including the minimum, maximum, and desired number of instances.

-asg-instance-screenshot.png: Displays a screenshot of running instances in the Auto Scaling Group.

-alb-traffic-distribution.png: Demonstrates the round-robin traffic distribution through the Application Load Balancer (ALB) to different web server instances.

-alb-dns-screenshot.png: Shows the DNS address of the Application Load Balancer and verifies that the website is accessible via the ALB.

------------------------------------------------------
# Configuration Files:
- nginx-setup.sh: Script to install and configure NGINX on EC2 instances.
- s3-bucket-policy.json: Bucket policy to enable public read access.
