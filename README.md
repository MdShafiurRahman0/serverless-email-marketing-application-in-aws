# Serverless Email Marketing Application in AWS


#Description: 
This project involves creating a serverless email marketing application using AWS services such as SES (Simple Email Service), Lambda, S3, EventBridge, and IAM. The application is designed to handle email marketing campaigns, automating the process of sending emails, managing templates, and tracking email performance.



#Components and Architecture

#Service We'll Be Using   

![image](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/2c187e96-a034-4745-9cb6-b49d2742fc7a)



#Amazon Simple Email Service (SES):

Purpose: SES is used to send marketing emails to a list of recipients. It provides high deliverability rates and offers features such as email tracking and feedback loops.
Usage: Emails are sent via SES, which can handle high volumes and ensures emails reach the inbox.


#AWS Lambda:

Purpose: Lambda functions are used to process various tasks in the email marketing workflow, such as sending emails, managing email lists, and handling incoming events.
Usage: Lambda functions are triggered by events (e.g., new campaign creation, email send requests) and perform operations like reading templates from S3, sending emails through SES, and processing bounce and complaint notifications.


#Amazon S3:

Purpose: S3 is used to store email templates, campaign data, and logs.
Usage: Email templates are uploaded to S3 and read by Lambda functions. Campaign data (such as recipient lists and email content) is also stored in S3, allowing for easy access and management.


#Amazon EventBridge:

Purpose: EventBridge is used to handle event-driven workflows, ensuring that actions within the application trigger the appropriate Lambda functions.
Usage: Events such as new campaign creation, email sends, and email tracking (opens, clicks) are captured by EventBridge and routed to the correct Lambda functions for processing.


#AWS Identity and Access Management (IAM):

Purpose: IAM is used to manage access control and permissions for the various AWS services and resources involved in the application.
Usage: IAM roles and policies are set up to ensure that Lambda functions, SES, S3, and EventBridge have the necessary permissions to perform their tasks securely. Additionally, IAM integration with GitHub is used for deployment and CI/CD pipelines.
Workflow


#Project Overview:

Users create a new email campaign by uploading recipient lists and email content (templates) to S3.
An event is triggered in EventBridge, which activates a Lambda function to process the campaign data.


#Email Sending:

The Lambda function reads the email template and recipient list from S3, and sends emails using SES.
SES sends the emails and tracks delivery status, opens, clicks, bounces, and complaints.


#Event Handling:

Events such as email bounces, complaints, opens, and clicks are captured by SES and sent to EventBridge.
EventBridge routes these events to Lambda functions for processing, which can update campaign statistics and recipient lists in S3.


#Security and Management

#IAM Roles and Policies:
Secure access to resources using fine-grained IAM policies. Lambda functions have specific roles that grant only the permissions they need to interact with SES, S3, and EventBridge.


This serverless email marketing application leverages the scalability, flexibility, and cost-efficiency of AWS services to provide a robust solution for managing email campaigns.




![image](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/e026c0ac-156c-402f-a36b-c0124823d18c)



![image](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/d9bfb28c-253e-4a5b-8d74-049dc34873bf)


# Step 1: Create S3 Bucket with Name

![2024-06-24_17h07_04](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/05eb2499-dab6-4036-b18e-5072431c1e1a)


# Step 2:  Upload the Files

![2024-06-24_17h37_05](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/d43d3ba1-9980-4612-b422-206ba3d6baf7)



# Step 3: AWS SES follow the SS


![2024-06-24_18h28_28](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/05e38362-f3f2-4983-bac8-a85ee72634d7)


![2024-06-24_18h29_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/62ec7b3c-703f-4904-b75d-91f8c2d5ce5a)


![2024-06-24_18h31_00](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/1336b9e3-d572-497f-b19d-5af92bbdb3b5)


## Step 1: Verify the Emails

![2024-06-24_18h35_50](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a186683c-d4a8-429d-85bb-bc286cb00506)


![2024-06-24_18h32_42](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/247c234b-bb24-49ea-bc33-635c6b78681b)



## Step 1: Create the Identities

![2024-06-24_18h39_35](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/84189b2f-b058-4a32-b8f8-31d66ee63869)


## Step 1: Send the Test Email

![2024-06-24_18h42_00](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/25fafcad-b5c1-4061-9870-54c2e209c123)



![2024-06-24_18h42_59](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/b2f1d955-d66a-4e0b-b0a3-b9763c4b3816)


## Step 1: Create the Lambda Functions

![2024-06-24_18h51_50](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/2db44d80-e22f-4af6-9b46-8f2719581803)


![2024-06-24_18h52_10](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/73612d89-1cad-4899-ba5e-d3917216f17c)


## Step 1: Paste Lambda Function Python Code from the file 

![2024-06-24_18h54_48](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/adf3f3ab-50f1-48f0-8ff5-65a4769070f6)


![2024-06-24_19h43_47](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/172902eb-abd8-40c1-b95f-3287cfacac75)


## Step 1: Paste Lambda Function Test Event 

![2024-06-24_19h44_44](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/b4010f0f-7779-4aa1-b18c-a17c328e5db4)

![2024-06-24_19h46_01](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/cc47adec-6079-42b4-98eb-341101b3f78a)



## Step 1: Successfully tested the Event

![2024-06-24_19h49_10](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/ed815c23-bf8a-44c1-a4b9-fd9ac31663d4)


## Step 1: Creating IAM Role & Add Policy

![2024-06-24_19h53_54](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/4d3af022-9708-484b-9681-2b5444d91494)


![2024-06-24_19h54_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/4644a869-2f51-45f0-9b4a-029ec043d425)


![2024-06-24_19h56_39](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/656585b4-d196-441a-996e-c8d625376f87)


## Step 1: Add permissions in Policy 

![2024-06-24_23h04_38](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/86a86128-0974-442a-b3e6-c08a4e9e0ca2)


![2024-06-24_23h04_12](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/b0d4cbb6-8ad2-4183-9f35-5d32fff80de8)



## Step 1: Finally 


![2024-06-24_23h06_34](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/7724cae3-af9a-4657-aeeb-ea63e28567fc)



![2024-06-25_00h05_02](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/dd7ce9ed-bdcc-428b-9cf2-f84ad85a3314)


## Step 1: Add Policy 7 Test the Event 

![2024-06-25_00h05_19](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/844e6283-51c9-4453-8e69-42fdaa72164a)

![2024-06-25_00h07_40](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/946e1dc3-23a3-47a4-8def-0e8fe27f60b7)


## Step 1: Email Marketing Template has Sentto the mail

![2024-06-25_00h08_21](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/1a028a71-15c6-4a9b-8cac-7436a9b70873)


![2024-06-25_00h09_01](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/5337a64f-9ce8-40b0-810e-dfeaa9f0273e)



## Step 1: Create Eventbridge Schedule

![2024-06-25_09h01_32](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a04b8d29-804a-4713-af1b-7c4166ed2104)


![2024-06-25_09h05_43](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/433b8c44-ff53-4854-a0d5-31df371a9163)


![2024-06-25_09h07_14](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/18864808-c276-4c1f-92e5-8a28df432f9d)


![2024-06-25_09h07_50](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/ff501b91-508e-43ff-bb21-57f672941f7c)


![2024-06-25_09h11_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a25c29fe-7749-45c0-931f-85cf4b33dd5b)


![2024-06-25_09h11_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/74316a20-9ea4-422b-af62-2b543fb91aee)


![2024-06-25_09h11_22](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/a9a1aeec-2f18-485a-bb15-f54e552a31dc)


![2024-06-25_09h11_46](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/7e52549d-8103-492f-9e1e-c5a38ec2857e)


![2024-06-25_09h12_31](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/9ecdf6b6-3388-47f5-bf56-f9296735e8e1)


![2024-06-25_09h13_09](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/7d309cd8-4356-4a64-a695-8ccdbf0b4336)


![2024-06-25_09h13_20](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/dadddcf2-1b6a-49c4-944e-a15365800d3c)


## Step 1: Successfully sent the mail on Sheduled Time

![2024-06-25_09h15_37](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/305d1c96-7a0f-456c-b2b6-9264c0d7692d)


![2024-06-25_09h15_59](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/4b06241a-cd3c-45d7-abee-0c01d8ae550a)


## Step 1: CloudWatch, Let's see the Logs

![2024-06-25_09h18_25](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/aaf583a7-14ca-4626-8bae-cebdca590670)


![2024-06-25_09h19_33](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/18522f19-3bf6-4b78-a49d-a355a070b480)


![2024-06-25_09h21_06](https://github.com/MdShafiurRahman0/serverless-email-marketing-application-in-aws/assets/113176437/6dac1ff9-34a0-434a-ad86-16dd7354dbee)








### What I Learned from Building a Serverless Email Marketing Application

1. **AWS Services Integration**:
   - **SES**: Learned how to configure and use Amazon Simple Email Service for sending and tracking high volumes of emails.
   - **Lambda**: Gained experience in writing and deploying Lambda functions for various tasks like email sending, event handling, and data processing.
   - **S3**: Understood how to store and manage static assets like email templates and recipient lists in Amazon S3.
   - **EventBridge**: Learned to use EventBridge for creating event-driven architectures, ensuring seamless communication between different parts of the application.
   - **IAM**: Acquired knowledge about setting up IAM roles and policies to securely manage access to AWS resources.

2. **Serverless Architecture**:
   - Grasped the principles of serverless computing, including automatic scaling, pay-as-you-go pricing, and reduced operational overhead.
   - Implemented a fully serverless application, understanding how different AWS services can work together to build scalable and maintainable solutions.

3. **Event-Driven Programming**:
   - Gained experience in designing and implementing event-driven workflows, using EventBridge to trigger Lambda functions based on various events (e.g., new campaign creation, email interactions).

4. **Email Marketing Fundamentals**:
   - Learned the key aspects of email marketing, such as crafting effective email templates, managing recipient lists, and tracking email performance metrics (delivery, open rates, click-through rates).

5. **Security Best Practices**:
   - Implemented security best practices, such as using IAM for fine-grained access control, securing S3 buckets, and ensuring Lambda functions have the least privilege necessary.
   - Understood the importance of protecting sensitive data and managing permissions effectively.

6. **Continuous Integration and Deployment (CI/CD)**:
   - Integrated IAM with GitHub to automate the deployment process, ensuring that code changes are automatically tested and deployed.
   - Learned about setting up CI/CD pipelines to streamline development workflows and improve code quality.

7. **Scalability and Performance Optimization**:
   - Understood how to design an application that can handle varying loads by leveraging the scalability features of AWS services.
   - Optimized performance by using asynchronous processing and efficient data handling techniques.

8. **Cost Management**:
   - Learned to manage and monitor AWS costs by understanding the Free Tier limits and optimizing resource usage.
   - Implemented cost-effective solutions by choosing the right services and configurations.

Building this serverless email marketing application provided a comprehensive understanding of various AWS services and how to leverage them to create scalable, efficient, and secure applications. This experience has enhanced my skills in cloud architecture, event-driven programming, and serverless computing.
