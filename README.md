# Blog-Generation-Using-AWS-Bedrock

This is an end to end GenAI project to generate blogs based on the provided title by the user. 
In this project we have created a lambda function that interacts with all the services and provide us with the final output stored in an s3 bucket
The project utilizes llama3 (llama3-8b-instruct) model from AWS Bedrock foundatuional models
We are utilizing the Postman to invoke a lambda function vai AWS API Gateway that generates the blog using AWS Bedrock and store it in an s3 bucket.
You can also create a frontend app to invoke the function and to display the results of generated blog as per your need but the frontend is not covered in the scope of this project

Following services are being used for this Project:

1) AWS API Gateway- To handle incoming API request
2) Lambda Function- To process the request and generate the response using bedrock
3) AWS Bedrock- To utilize the foundational LLM models (llama3 in this case)
4) s3 Bucket- To store the genrarted blogs
5) AWS CloudWatch- Default logging of lambda functions 

# Note:
    We have created a custom layer for lambda function to utilize the latest version of boto3 library.
    In order to create a custom layer you have to make a folder with name "python" and install all the dependencies inside that folder. For example in our case we will use:
    
    pip install boto3 -t python/

    After the installation we can package the entire folder in zip file and can use it as a layer in our lambda function
