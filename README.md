# AWS Certified Developer – Associate tips

## VPC

- There can be only one route table per subnet.

## IAM

- If you are connecting to AWS from a computer, not an EC2 instance, you need to create an AWS user, attach permissions, and use the API access key and secret access key in your code. 

## EC2

- AMIs can be shared to individual AWS accounts.

- AMI’s can only be shared within a region. To make them available across regions , you need to copy them across regions.


## S3

- Any objects uploaded prior to versioning will have the version ID as NULL.

- Multi-Object Delete can be used to delete a large number of objects.

- x-amz-server-side-encryption will cause an object to be SSE.

- 100 is the maximum number of S3 buckets by default allowed per AWS account.

## SNS

- Name, type, and value must not be empty or null and the message body shouldn't be empty or null either.

## SQS

- If long polling is enabled the reader will listen to the queue until a message is available or until timeout.

- AWS SQS is PCI DSS certified.

- 1 million requests are allowed in the free tier.

- the maximum visibility timeout is 12 hours.

- There is no limit on the number of queues.

- SQS queues can deliver the message more than one, and the order of messages is not defined.

- SQS max message size is 256KB. To send bigger messages use the Amazon SQS Extended Client Library for Java.

- Long polling makes it inexpensive to retrieve messages from your Amazon SQS queue as soon as the messages are available. Using long polling might reduce the cost of using SQS, because you can reduce the number of empty receives To enable long polling you need to set the value of ReceiveMessageWaitTimeSeconds to greater than 0 and less than or equal to 20 seconds.
