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

- Multi-part upload API allows you to stop and resume uploads

- Multi-Object Delete can be used to delete a large number of objects.

- Parts of a multi-part upload will not be completed until the "complete" request has been called which puts all the parts of the file together.

- S3 object key names are stored lexicographically.

- A benefit of multi-part upload is that you can upload a file as it is being created.

- x-amz-server-side-encryption will cause an object to be SSE.

- 100 is the maximum number of S3 buckets by default allowed per AWS account.

- By default, all Amazon S3 resources—buckets, objects, and related subresources (for example, lifecycleconfiguration and website configuration)—are private.

- S3 bucket policies require a Principal be defined.

- To host your static website, you configure an Amazon S3 bucket for website hosting and then upload your website content to the bucket. The website is then available at the region-specific website endpoint of the bucket: <bucket-name>.s3-website-<AWS-region>.amazonaws.com

## SNS

- Name, type, and value must not be empty or null and the message body shouldn't be empty or null either.

- SNS guarantee message delivery to SQS.

- SNS send to endpoints a JSON document with parameters like Message, Signature, Subject, Type.

- Topic names are limited to 256 characters.

- The time period available for confirmation is 3 days.

- Once a message has been published to SNS, it can not be recalled.

## DynamoDB

-  An atomic counter allows all write requests to be applied in the order they are received by incrementing or decrementing the attribute value.

- An item stored in a DynamoDB can contain any number of attributes associated to it.

 - DynamoDB does not support cross table joins

- Reads of a DynamoDB table are eventual consistency, unless you specify otherwise.

- For write capacity, the rule is to divide the item size by 1KB.

- For read capacity, the rule is to divide the item size by 4KB. 

- A DynamoDB table can contain 5 local secondary indexes on a table.

- DynamoDB uses optimistic concurrency control.

- Humans can not perform a decision task.

- 256 is the maximum number of tables per region.

- The cumulative number of tables and indexes in the CREATING, DELETING or UPDATING state cannot exceed 10.

- One DynamoDB read capacity unit represents one strongly consistent read per second, for an item up to 4 KB in size. 

- UpdateTable does not consume capacity units.

 You exceed your maximum allowed provisioned throughput for a table or for one or more global secondary indexes.

- Query and Scan both support eventual consistent reads.

- A local secondary index is an index that has the same hash key as the table, but a different range key.

- 5 local and 5 global secondary indexes are allowed , which gives a maximum of 10 per table.

- The BatchGetItem operation returns the attributes of one or more items from one or more tables. You identify requested items by primary key.

- A Query operation uses the primary key of a table or a secondary index to directly access items from that table or index.

-  A local secondary index has the same partition key as the primary key and the global secondary index can have different partition and sort key.

- DynamoDB uses conditional writes for consistency.

- DynamoDB does not allow secondary index limit increase.

- To help clients coordinate writes to data items, DynamoDB supports conditional writes for PutItem, DeleteItem, and UpdateItem operations. With a conditional write, an operation succeeds only if the item attributes meet one or more expected conditions; otherwise it returns an error.

- 5 global security indexes are allowed.

- All scalar data types can be indexed.

- An index can not be modified after creation.

- 400KB is the maximum size of an item in DynamoDB.

- By default, AWS allows you to have 256 DynamoDB tables per account, per region. 

- 10GB is maximum limit for the size of an item collection in DynamoDB.

- 100 is the smallest amount of reserved capacity that can be purchased for DynamoDB.

- There is no limit to the number of attributes an item can have in DynamoDB

## SWF

- The maximum number of SWF domains allowed in an AWS account is 100.

- A SWF workflow task or task execution can live up to 1 year.

- It guarantees delivery order of messages/tasks.

- Video encoding is one of the major use cases for using SWF.

- Domains are the containers called for segregating application resources.

## SQS

- If long polling is enabled the reader will listen to the queue until a message is available or until timeout.

- Messages will be delivered one or more times, and message delivery order is indeterminate.

- SQS guarantees delivery but there can be duplicates.

- 30 seconds is the default timeout for visibility queue in SQS.

- AWS SQS is PCI DSS certified.

- 1 million requests are allowed in the free tier.

- The maximum visibility timeout is 12 hours.

- There is no limit on the number of queues.

- SQS queues can deliver the message more than one, and the order of messages is not defined.

- SQS max message size is 256KB. To send bigger messages use the Amazon SQS Extended Client Library for Java.

- Long polling makes it inexpensive to retrieve messages from your Amazon SQS queue as soon as the messages are available. Using long polling might reduce the cost of using SQS, because you can reduce the number of empty receives To enable long polling you need to set the value of ReceiveMessageWaitTimeSeconds to greater than 0 and less than or equal to 20 seconds.

## Cloud Formation

- AWS CloudFormation assume default template version if one is not explicitly mentioned in a CloudFormation template.
- It provides a set of Python helper scripts that you can use to install software and start services on an Amazon EC2 instance in your stack.

- There are no limits to the number of templates.

- You can use intrinsic functions only in specific parts of a template. Currently, you can use intrinsic functions in resource properties, outputs, metadata attributes, and update policy attributes. You can also use intrinsic functions to conditionally create stack resources.

- Resources is the only mandatory field.
