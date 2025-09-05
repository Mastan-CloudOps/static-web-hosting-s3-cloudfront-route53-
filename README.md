  Static Website Hosting on AWS (S3 + CloudFront + Route 53)

This project demonstrates how to host a static website on AWS S3 with CloudFront CDN and Route 53 DNS.

Project Structure

├── README.md
└── website
    ├── index.html
    └── error.html

Project Overview
       Frontend: Static HTML files.
       Storage: AWS S3 (bucket stores website files)
       CDN: CloudFront (distributes content globally)
       DNS: Route 53 (maps domain name to CloudFront)

  Steps to Deploy  

1. Prepare Website Files
2. Create an S3 Bucket  -----> S3 → Create Bucket ---> Bucket name: md-static-website- ----> Region: ap-south-1 ---> Block Public Access: **ON** (keep bucket private)
3. Create CloudFront Distribution ----> CloudFront → Create Distribution ---> Origin domain: Select your S3 bucket ---> Origin Access: Create **Origin Access Control (OAC) ---->                                                   Set Viewer Protocol Policy: Redirect HTTP → HTTPS -----> Default root object: index.html
4. Secure S3 Bucket with OAC ---> Go to bucket → Permissions → Bucket Policy → Add generated policy
5. Configure DNS (Route 53)
