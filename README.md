🛍️ ShopSmart — Serverless E-Commerce Demo

ShopSmart is a fully serverless e-commerce demo application built on AWS, designed to showcase a modern cloud-native shopping experience.

It demonstrates how to build a real-world serverless system using:

✨ AWS Lambda
✨ Amazon API Gateway
✨ Amazon DynamoDB
✨ Amazon S3 (static hosting)
✨ IAM
✨ AWS CloudShell (full development environment)

🌐 Live Demo
Frontend (S3 static website)

🔗 http://shopsmart-hkilla-2025.s3-website-us-east-1.amazonaws.com


🏗️ Architecture Overview
Frontend

Single-page app (index.html) using HTML, CSS, and JavaScript

Hosted on Amazon S3 static website hosting

Communicates with API Gateway to load products and handle cart operations

Backend
Amazon API Gateway (REST)

GET /products → loads product catalog from DynamoDB via Lambda

AWS Lambda (Python)

Runtime: Python 3.x

Reads from DynamoDB table ShopSmartProducts

Converts DynamoDB Decimal types to standard JSON numbers

Returns a list of product objects as JSON

Amazon DynamoDB

Example table items:

[
  {
    "productId": "laptop-stand",
    "name": "Laptop Stand",
    "description": "Adjustable laptop stand with Per Scholas logo",
    "price": 50
  },
  {
    "productId": "laptop",
    "name": "Laptop",
    "description": "High-performance laptop with AWS Lambda logo",
    "price": 1200
  }
]

🗂️ Repository Structure
ShopSmart/
│
├── index.html                 # Frontend UI
├── thankyou.html              # Order confirmation page
│
├── shopsmart-assets/          # Images and assets
│   ├── shopsmart-logo.png
│   ├── laptop_aws_lambda_logo.jpg
│   └── laptop_stand_per_scholas_logo.jpg
│
├── lambda/
│   ├── lambda_function.py     # Backend product loader
│   ├── response.json
│   └── function.zip           # Deployment package
│
└── public-read-policy.json    # S3 bucket policy

🚀 Deployment Flow (AWS CloudShell)

Create S3 bucket

Upload frontend and set bucket policy

Deploy Lambda + API Gateway

Insert products into DynamoDB

Visit the live website

👤 Author

Hawi Jordan, Amarachi Emeziem, Rory Mclean, MD Shohel Khan (Sohel), Olusegun Ajayi-Johnson

AWS Cloud Engineer • AWS Serverless Builder

🔗 GitHub: https://github.com/HawiK285

🔗 LinkedIn: www.linkedin.com/in/hawi-jordan-3b18752a9
