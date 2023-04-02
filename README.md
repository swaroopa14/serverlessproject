
# Building a Telegram Bot with AWS API Gateway, AWS Lambda, and Postman
What is AWS Lambda?
AWS Lambda is a serverless computing service provided by Amazon Web Services (AWS) that allows developers to run code without provisioning or managing servers. With Lambda, developers can upload their code in the form of functions, and Lambda will automatically handle the rest, including scaling, patching, and monitoring.
What is API Gateway?


API Gateway is a managed service offered by AWS that allows developers to create, deploy, and manage APIs for their applications. It acts as a "front door" to backend services, providing a secure and scalable API layer for client applications. API Gateway supports a variety of API types and provides features such as caching, authentication, and rate limiting to manage API traffic and improve performance. It can also integrate with other AWS services, such as Lambda and IAM, to provide additional functionality. API Gateway is a powerful platform for building APIs that are scalable, secure, and easy to manage.
The Architectural Workflow
create a telegram bot that will be hosted on the server side now suppose any user if they are publishing a message in that particular bot using telegram OVO what will happen means the message will be pushed to our client system.
In AWS we basically exposed that particular post API using Amazon API Gateway and from that API Gateway, we can trigger and also process that particular message and return some responsive message to our server. 
The user will publish an URL to our telegram bot so what will happen is we will be setting up one webhook here so the telegram bot will push that particular event to our post API endpoint which is hosted using API Gateway from that API Gateway it will be triggered to Lambda.
Lambda will call a third-party API which is basically a clean URL API that is nothing but can act like an ewall shortener.
Suppose the user is passing a very big URL and you want to get back a very short URL then you can use this particular API we will call this particular API using python code which is running in Lambda and then we will shorten our URL which is shared by the user we will get back the response in Lambda and from Lambda we will push that to our telegram server from where user can get the short format of the URL.
