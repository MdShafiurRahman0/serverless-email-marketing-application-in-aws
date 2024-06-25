# Architeture


## Amazon Simple Email Service (SES): 

Purpose: SES is used to send marketing emails to a list of recipients. It 
provides high deliverability rates and offers features such as email tracking 
and feedback loops. 

Usage: Emails are sent via SES, which can handle high volumes and ensures 
emails reach the inbox. 


## AWS Lambda 

Purpose: Lambda functions are used to process various tasks in the email 
marketing workflow, such as sending emails, managing email lists, and 
handling incoming events. 

Usage: Lambda functions are triggered by events (e.g., new campaign creation, 
email send requests) and perform operations like reading templates from S3, 
sending emails through SES, and processing bounce and complaint 
notifications. 


## Amazon S3 

Purpose: S3 is used to store email templates, campaign data, and logs. 

Usage: Email templates are uploaded to S3 and read by Lambda functions. 
Campaign data (such as recipient lists and email content) is also stored in 
S3, allowing for easy access and management. 


## Amazon EventBridge 

Purpose: EventBridge is used to handle event-driven workflows, ensuring that 
actions within the application trigger the appropriate Lambda functions. 

Usage: Events such as new campaign creation, email sends, and email tracking (
opens, clicks) are captured by EventBridge and routed to the correct Lambda 
functions for processing. 


## AWS Identity and Access Management (IAM) 

Purpose: IAM is used to manage access control and permissions for the various 
AWS services and resources involved in the application. 

Usage: IAM roles and policies are set up to ensure that Lambda functions, 
SES, S3, and EventBridge have the necessary permissions to perform their 
tasks securely. Additionally, IAM integration with GitHub is used for 
deployment and CI/CD pipelines. 
