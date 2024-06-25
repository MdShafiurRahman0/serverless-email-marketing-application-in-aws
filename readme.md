# Serverless Email Marketing Application in AWS

**Description:**

This project involves creating a serverless email marketing application using 
AWS services such as SES (Simple Email Service), Lambda, S3, EventBridge, and 
IAM. The application is designed to handle email marketing campaigns, 
automating the process of sending emails, managing templates, and tracking 
email performance. 


## Components and Architecture

![image](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/2c187e96-a034-4745-9cb6-b49d2742fc7a)

Service We'll Be Using. You can read more about [here](./docs/architecture.md).


##  Workflow

**Project Overview:** 

Users create a new email campaign by uploading recipient lists and email 
content (templates) to S3. 

An event is triggered in EventBridge, which activates a Lambda function to 
process the campaign data. 


**Email Sending:** 

The Lambda function reads the email template and recipient list from S3, and 
sends emails using SES. 

SES sends the emails and tracks delivery status, opens, clicks, bounces, and 
complaints. 


**Event Handling:** 

Events such as email bounces, complaints, opens, and clicks are captured by 
SES and sent to EventBridge. 

EventBridge routes these events to Lambda functions for processing, which can 
update campaign statistics and recipient lists in S3. 


**IAM Roles and Policies (Security and Management )** 

Secure access to resources using fine-grained IAM policies. Lambda functions 
have specific roles that grant only the permissions they need to interact 
with SES, S3, and EventBridge. 


This serverless email marketing application leverages the scalability, 
flexibility, and cost-efficiency of AWS services to provide a robust solution 
for managing email campaigns. 

![image](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/e026c0ac-156c-402f-a36b-c0124823d18c)

![image](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/d9bfb28c-253e-4a5b-8d74-049dc34873bf)


## How to build it

You can following this [steps](./docs/build.md).

