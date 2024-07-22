# Social-Media-Hashtag-Trend-Analyzer-Application

To meet the demand for seamless social media experiences, we are developing a Streamlit app that lets users compose and publish posts, similar to popular social platforms. This app integrates with AWS Lambda and DynamoDB for efficient post processing and hashtag analysis.

## 1. Import Libraries
The app begins by importing necessary libraries:

1.streamlit for the web interface. 
2.boto3 for AWS interactions. 
3.uuid for generating unique identifiers. 
4.requests for making HTTP requests. 
5.json for handling JSON data. 

## 2. AWS Configuration
1.Set up AWS credentials and configuration parameters  
2.Access keys and secret keys for authentication. 
3.The AWS region where your resources are located. 
4.The Lambda function name and the API Gateway endpoint for posting data. 

## 3. Initialize AWS Clients
Initialize the DynamoDB client to interact with the DynamoDB table and the Lambda client. 

## 4. Streamlit UI Components
1.Create the user interface using Streamlit 
2.Title for the Post Compose. 
3.Input fields for post content and hashtags. 

## 5. Publish Button Functionality
1.Add a button to publish posts 
2.Validate that post content and hashtags are provided. 
3.Prepare the post data with a unique post ID and a list of hashtags. 
4.Send the post data to AWS Lambda via the API Gateway. 
5. Handle the response to display success or error messages. 

## 6. Display Trending Hashtags
1.Add a section to display trending hashtags 
2.Button to fetch and display trending hashtags. 
3.Query the DynamoDB table to get all posts. 
4.Count the occurrences of each hashtag. 
5.Sort and display the top 3 trending hashtags. 
6.AWS Lambda Function (PostProcessorFunction) 
7.The Lambda function is designed to handle post submissions: 

# AWS Lambda Function (PostProcessorFunction)
## The Lambda function is designed to handle post submissions:

## Initialize DynamoDB Resource: Set up DynamoDB to interact with the 'Trend' table.
## Extract Post Data:Parse the incoming event data to extract the post details.
## Prepare and Store Item:Create an item with the post details and store it in DynamoDB.
## Return Response:
## Return a success response if the post is processed correctly.
## Return an error response if there is an issue processing the post.
