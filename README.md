# Cloud API Resume with AWS.

This project is a version of the popular Cloud Resume Challenge, but with an exciting twist. Here are some differences:
- Instead of manually deploying resources on the AWS Management Console, we will use Infrastructure as Code(IaC). Click [here](https://learn.microsoft.com/en-us/devops/deliver/what-is-infrastructure-as-code) to learn more about IaC.
- We shall use different services. We will use a Lambda function and API Gateway to deliver your resume as a JSON document.

This project is beginner friendly, and will help you gain hands-on skills in the AWS Cloud Platform. 

## Prerequisites
Here's what you will need to complete this project:
- - An AWS [account](https://aws.amazon.com/resources/create-account/)
- - Terraform. Download it [here](https://www.terraform.io/)

## Architecture Diagram

![Cloud Resume API (2)](https://github.com/user-attachments/assets/70e7cb43-06fd-43dd-8b2f-da76c45f8523)

### How It Works.
- **API Gateway**: Routes requests to the AWS Lambda function.
- **AWS Lambda**: Executes serverless code to fetch resume data from DynamoDB based on the provided ID, and returns it in JSON format.
- **DynamoDB**: A NoSQL database that stores and organizes resume data in a structured format for efficient retrieval by the Lambda function.
- **S3**: Hosts static assets created with React for the frontend. These assets interact with the API Gateway to fetch and display resume data.
- **CloudFront**: Distributes and caches the static frontend assets from the S3 bucket, providing low-latency access and improving the overall performance of the website.

**API Endpoint**:
```
https://u7fdthk4r6.execute-api.eu-north-1.amazonaws.com/dev/
```
