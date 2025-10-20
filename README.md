# 🚀 Serverless Cloud Dictionary
Serverless Dictionary API with AWS Components

## Short Description
A fully cloud-native dictionary lookup service built on AWS. It exposes a REST API for querying definitions of terms, using a serverless backend (Lambda + API Gateway) and a DynamoDB table for storage — enabling efficient, scalable and cost-effective dictionary lookups.

## 🛠️ AWS Services Used:
Amazon API Gateway,
AWS Lambda,
Amazon DynamoDB,
Amazon S3 (optional for static assets),
AWS IAM,

## 🧰 Technical Tools:
Python (or Node.js) for Lambda functions,
Boto3 (or AWS SDK) for AWS service integration,
Serverless Framework or AWS SAM (optional)

## 🧠 Skills Demonstrated:
Serverless architecture design,
REST API implementation with AWS,
DynamoDB design & usage,
Cloud-native deployment and scalability

## 📋 Steps Performed

### Create DynamoDB Table:
Created a DynamoDB table named CloudDictionary with term as the partition key.
Populated the table with dictionary entries (terms and their definitions) for querying.

### Deploy Lambda Function:
Created an AWS Lambda function (e.g., getDefinitionFunction) using Python or Node.js runtime.
Configured the Lambda to read definitions from the DynamoDB table based on the requested term.

### Configure API Gateway:
Created a REST API in API Gateway with a GET endpoint (for example /define/{term}).
Connected the endpoint to the Lambda function as the backend integration.
Set up request/response mapping so users can submit a term and receive its definition.

### Set IAM Permissions and Roles:
Created an IAM role for the Lambda with permissions to read from the DynamoDB table.
Configured necessary execution roles for API Gateway and Lambda to operate securely.

### Deploy and Test the API:
Deployed the API Gateway to a stage (e.g., prod).
Tested the endpoint with sample terms to verify correct definitions are returned.
Verified edge cases (term not found, invalid input) to ensure graceful error handling.

## ✅ Final Result:
Serverless Dictionary Lookup Service

##  💼 Business Implication:
This project illustrates how to build a scalable, cost-effective dictionary service using AWS’s serverless stack. Organizations can provide real-time definition lookup functionality without managing servers, and the architecture scales automatically with usage — making it ideal for education platforms, content services, or API-first products requiring minimal infrastructure overhead.
