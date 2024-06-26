# secure-aws-api

Project: Setting up Secure Authentication to AWS API

1. Steps to Set Up Secure Authentication



Step 1: Obtain AWS Credentials



•	I came to the AWS Management Console and navigate to IAM (Identity and Access Management).



•	I create a new IAM user or use an existing one.



•	Attach a policy (e.g., AmazonS3ReadOnlyAccess) to the IAM user based on the API service you want to access.



•	Note down the Access Key ID and Secret Access Key for this IAM user.



Step 2: Set Up AWS SDK or API Client




•	Install the AWS SDK or API client for your programming language (e.g., boto3 for Python, AWS SDK for JavaScript).



•	Configure the SDK with your AWS credentials:



o	Provide the Access Key ID and Secret Access Key.



Step 3: Sign Your API Requests



•	I constructed  the request according to the AWS service API documentation.



•	Signed the request using AWS Signature Version 4. This involves:



o	Computing a cryptographic hash (SHA-256) of your request payload.



o	Constructing a canonical request string with specific headers, HTTP method, etc.


o	Generating a string to sign using your AWS credentials.



o	Computing the signature using the generated string to sign and including it in the request headers.




Step 4: Send the Signed Request



•	I inncluded the generated AWS Signature Version 4 in the HTTP headers of your request.



•	I sent the request to the AWS API endpoint.




2. Testing and Troubleshooting



•	I tested your API requests to ensure they are authenticated correctly.




•	I checked AWS CloudTrail logs for any authentication-related errors.



•	I proceeded to monitor AWS IAM for any permission issues or security concerns.



•	I used IAM Roles: For EC2 instances or other AWS resources, use IAM roles instead of IAM user credentials for better security.



•	I made sure credentials  regularly rotate your AWS credentials to enhance security.


•	Use HTTPS: Always use HTTPS when making API requests to encrypt data in transit


I have learnt a lot from this project.


