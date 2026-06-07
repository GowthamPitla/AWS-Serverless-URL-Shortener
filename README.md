# AWS Serverless URL Shortener

A cloud-native URL shortening service built using AWS Serverless technologies. This application converts long URLs into short, shareable links and redirects users to the original destination using a scalable, event-driven architecture.

## 🚀 Overview

The AWS Serverless URL Shortener leverages AWS services to provide a highly available and cost-effective URL shortening platform. The application follows a serverless architecture, eliminating the need for server management while ensuring automatic scaling and high performance.

## ✨ Features

* Generate unique short URLs from long URLs
* Redirect users to the original URL
* RESTful API architecture
* Serverless and scalable design
* Fast URL lookup using DynamoDB
* Infrastructure as Code (IaC) with CloudFormation
* Logging and monitoring with CloudWatch
* Secure resource access using IAM roles and policies

## 🛠️ Tech Stack

### Cloud Services

* AWS Lambda
* Amazon API Gateway
* Amazon DynamoDB
* AWS IAM
* Amazon CloudWatch
* AWS CloudFormation

### Backend

* Python
* REST APIs
* JSON

## 🏗️ Architecture

```text
User Request
      │
      ▼
Amazon API Gateway
      │
      ▼
 AWS Lambda Function
      │
      ▼
 Amazon DynamoDB
      │
      ▼
 Return Short URL
```

### URL Redirection Flow

```text
Short URL Request
        │
        ▼
 Amazon API Gateway
        │
        ▼
 AWS Lambda Function
        │
        ▼
 DynamoDB Lookup
        │
        ▼
 Redirect to Original URL
```

## 📂 Project Structure

```text
aws-serverless-url-shortener/
│
├── lambda/
│   ├── create_url.py
│   ├── redirect_url.py
│
├── cloudformation/
│   └── infrastructure.yaml
│
├── tests/
│   └── test_api.py
│
├── README.md
└── requirements.txt
```

## ⚙️ Installation & Deployment

### Clone the Repository

```bash
git clone https://github.com/GowthamPitla/aws-serverless-url-shortener.git
cd aws-serverless-url-shortener
```

### Deploy Using CloudFormation

```bash
aws cloudformation deploy \
--template-file infrastructure.yaml \
--stack-name url-shortener-stack
```

### Configure API Gateway

* Create API endpoints
* Integrate Lambda functions
* Deploy API stage

## 📌 API Endpoints

### Create Short URL

```http
POST /shorten
```

Request:

```json
{
  "url": "https://example.com/very-long-url"
}
```

Response:

```json
{
  "short_url": "https://xyz.ly/a1b2c3"
}
```

### Redirect URL

```http
GET /{shortCode}
```

Response:

```http
302 Redirect
```

## 🔒 Security Features

* IAM-based access control
* Input validation
* Error handling and logging
* Secure API integration

## 📊 Monitoring

Amazon CloudWatch is used to:

* Track API requests
* Monitor Lambda execution
* Log application events
* Detect failures and exceptions

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

* AWS Serverless Architecture
* AWS Lambda Functions
* API Gateway Integration
* DynamoDB Data Modeling
* Infrastructure as Code (CloudFormation)
* Cloud Monitoring and Logging
* REST API Development
* Cloud-Native Application Design

## 🔮 Future Enhancements

* User Authentication using AWS Cognito
* URL Analytics Dashboard
* Custom URL Aliases
* URL Expiration Feature
* QR Code Generation
* Click Tracking and Reporting

## 👨‍💻 Author

**Gowtham Pitla**

B.Tech – Artificial Intelligence & Data Science

AWS Certified Cloud Practitioner | AWS Certified AI Practitioner

Passionate about Cloud Computing, Backend Development, and Scalable Software Systems.
