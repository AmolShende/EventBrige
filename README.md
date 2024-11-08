# EventBrige
Will Terminate EC2 If we create large configuration instance through Lambda and EventBridge  ( Will create t2.micro for testing)

1) create an IAM role and assign lambda service two roles - AmazonEC2FullAccess and AWSLambdaBasicExecutionRole
2) create a lambda function with this role and use the terminate-ec2.py script to terminate the ec2 instance.
3) create a EventBridge rule to trigger the above lambda on the "EC2 Instance state change event".
4) Verify by starting a ec2 intance and then it will be automatically terminated.
