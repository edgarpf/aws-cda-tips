# AWS Certified Developer – Associate tips

## General

- Default region is us-east-1.

- It is possible to transfer a reserved instance from one Availability Zone to another.

- Fanout is one of the common pattern scenario’s when it comes to the combination of SNS and SQS. In this pattern, a message published to an SNS topic is distributed to a number of SQS queues in parallel. By using this pattern, you can build applications that take advantage parallel, asynchronous processing.

## VPC

- There can be only one route table per subnet.

- A subnet can not be associated with multiple Access Control Lists.

- You can create 200 subnets per vpc.

- You can have 5 VPC's per region.

- You can attach only one internet gateway to a custom VPC.

## ELB

- You can have multiple SSL certificates (for multiple domain names) on a single Elastic Load Balancer.

## EBS

- 10 GiB is the size limit for volumes in instances that are based on Amazon Instance Store backed AMI’s.

- BundleInstance is used to Bundle an Amazon instance store-backed Windows instance.

- The instance type and kernel for an EBS backed AMI can easily be changed as compared to an Instance store-backed AMI.

## IAM

- If you are connecting to AWS from a computer, not an EC2 instance, you need to create an AWS user, attach permissions, and use the API access key and secret access key in your code. 

## EC2

- AMIs can be shared to individual AWS accounts.

- AMI’s can only be shared within a region. To make them available across regions , you need to copy them across regions.

## AS

-  There are no charges for using the Autoscaling service.

## S3

- Any objects uploaded prior to versioning will have the version ID as NULL.

- Multi-part upload API allows you to stop and resume uploads

- Multi-Object Delete can be used to delete a large number of objects.

- Parts of a multi-part upload will not be completed until the "complete" request has been called which puts all the parts of the file together.

- The object creation REST APIs provide a request header, x-amz-server-side-encryption that you can use to request server-side encryption.

- S3 object key names are stored lexicographically.

- A benefit of multi-part upload is that you can upload a file as it is being created.

- x-amz-server-side-encryption will cause an object to be SSE.

- 100 is the maximum number of S3 buckets by default allowed per AWS account.

- By default, all Amazon S3 resources—buckets, objects, and related subresources (for example, lifecycleconfiguration and website configuration)—are private.

- S3 bucket policies require a Principal be defined.

- To host your static website, you configure an Amazon S3 bucket for website hosting and then upload your website content to the bucket. The website is then available at the region-specific website endpoint of the bucket: <bucket-name>.s3-website-<AWS-region>.amazonaws.com

## SNS

- SNS guarantee message delivery to SQS.

- It is push based.

- A JSON object containing MessageId, unsubscribeURL, Subjec is the format of structured notification messages sent by Amazon SNSt, Message and other values.

- Name, type, and value must not be empty or null and the message body shouldn't be empty or null either.

- 100,000 is the maximum number of topics allowed per account in SNS.

- Subject, Message and Format are valid arguments for an SNS Publish request.

- SNS send to endpoints a JSON document with parameters like Message, Signature, Subject, Type.

- Topic names are limited to 256 characters.

- The time period available for confirmation is 3 days.

- Once a message has been published to SNS, it can not be recalled.

## DynamoDB

-  An atomic counter allows all write requests to be applied in the order they are received by incrementing or decrementing the attribute value.

- You can increase Provisioned throughput limits by raising a ticket to AWS support

- The BatchGetItem operation returns the attributes of one or more items from one or more tables.

- A scan is not more efficient than a query in terms of performance.

- BatchGetItem is the API call to retrieve multiple items from a DynamoDB table.

- Set a smaller page size for the scan can be used to minimize the impact of a scan on a table’s provisioned throughput.

- One DynamoDB strongly consistent read capacity unit is equal to two eventual consistent read per second.

- An item stored in a DynamoDB can contain any number of attributes associated to it.

- Strongly consistent reads uses more provisioned read throughput than eventually consistent reads.

- You can not select a specific Availability Zone in which to place your DynamoDB Table.

- DynamoDB does not support cross table joins

- It supports two types of primary keys: Hash and hasn and Range.

- Reads of a DynamoDB table are eventual consistency, unless you specify otherwise.

- For write capacity, the rule is to divide the item size by 1KB.

- Expressions can be used in DynamoDB as part of the Query API call to filter results based on the values of primary keys.

- 100 is the maximum number of items that the BatchGetItem API retrieve from DynamoDB.

- A global secondary index can becreated at the same time as the table creation

- A Global Secondary Index can have different partition key and sort key from those of its base table.

- 1 MB is the maximum limit of data that can be retrieved by a scan operation in DynamoDB.

- A local secondary index has the same partition key as the primary key.

- For read capacity, the rule is to divide the item size by 4KB. 

- A DynamoDB table can contain 5 local secondary indexes on a table.

- DynamoDB uses optimistic concurrency control.

- DynamoDB uses conditional writes for consistency.

- Humans can not perform a decision task.

- 256 is the maximum number of tables per region.

- The cumulative number of tables and indexes in the CREATING, DELETING or UPDATING state cannot exceed 10.

- One DynamoDB read capacity unit represents one strongly consistent read per second, for an item up to 4 KB in size. 

- UpdateTable does not consume capacity units.

- You exceed your maximum allowed provisioned throughput for a table or for one or more global secondary indexes.

- Query and Scan both support eventual consistent reads.

- A local secondary index is an index that has the same hash key as the table, but a different range key.

- 5 local and 5 global secondary indexes are allowed , which gives a maximum of 10 per table.

- The BatchGetItem operation returns the attributes of one or more items from one or more tables. You identify requested items by primary key.

- "ProvisionedThroughputExceededException" error is caused due to the following reason: You exceeded your maximum allowed provisioned throughput for a table or for one or more global secondary indexes. 

- Each table can have up to 5 local secondary indexes.

- There is no limit to a table size.

- A Query operation uses the primary key of a table or a secondary index to directly access items from that table or index.

-  A local secondary index has the same partition key as the primary key and the global secondary index can have different partition and sort key.

- Atomic counters can be used to increment or decrement the value of an existing attribute without interfering with other write requests.

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

- Flow Framework helps in developing Amazon SWF based applications.

- SWF uses deciders and workers to complete tasks.

- 1000 is the maximum number of open activity tasks.

- SWF tasks are assigned once and never duplicated.

- You can have a maximum of 10,000 workflow and activity types (in total) that are either registered or deprecated in each domain. You can have a maximum of 100 Amazon SWF domains (including registered and deprecated domains) in your AWS account.

- It guarantees delivery order of messages/tasks.

- Video encoding is one of the major use cases for using SWF.

- Domains are the containers called for segregating application resources.

## SQS

- SQS was the first service on the AWS platform

- If long polling is enabled the reader will listen to the queue until a message is available or until timeout.

- 1KB is the minimum value that can be configured for Amazon SQS MaximumMessageSize attribute.

- There is no limit on the number of queues.

- To enable long polling u need to set the value of ReceiveMessageWaitTimeSeconds to greater than 0 and less than or equal to 20 seconds.

- SQS long polling costs the same that short polling

- Amazon SQS long polling is a way to retrieve messages from your Amazon SQS queues. While the regular short polling returns immediately, even if the message queue being polled is empty, long polling doesn’t return a response until a message arrives in the message queue, or the long poll times out.

- 256KB is the maximum size of SQS message.

- 256 characters is the maximum length of a topic name in SNS.

- Messages will be delivered one or more times, and message delivery order is indeterminate.

- SQS guarantees delivery but there can be duplicates.

- Dead letter queues handles unsuccessfully-processed messages in SQS.

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

- 60 is the limit to the number of parameters in the template.

- The valid parts of the Cloud Formation template are parameters, outputs and resources.

- There are no limits to the number of templates.

- You can use intrinsic functions only in specific parts of a template. Currently, you can use intrinsic functions in resource properties, outputs, metadata attributes, and update policy attributes. You can also use intrinsic functions to conditionally create stack resources.

- Resources is the only mandatory field.
