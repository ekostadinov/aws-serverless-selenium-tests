# AWS Serverless Selenium Tests

## Event Description

We are going to talk about:

1. Migration Away From Traditional Infrastructure

2. Serverless Architecture and Framework

3. Selenium Tests Solution

4. Managing Your SLS Solution

## Update: Serverless Framework & Batch

It is possible to leverage your setup by combining Serverless framework and AWS Batch (retire Terraform as Config management). There are two options in theory, but one in practice:

 1. [serverless-aws-batch](https://github.com/justinram11/serverless-aws-batch) NPM pack (I don't recommend it, as it is not part of the `sls plugin list | grep batch` and is quite unknown)
 
 2. AWS [Step Functions](https://github.com/ryfeus/stepfunctions2processing#aws-batch-example), which allow us to run hybrid serverless/cluster workflows. Meaning we can have better code decomposition via AWS Lambda and AWS Batch for processing, and 
Serverless framework for handling deployment and configuration. Our `functions` which contain information about the Lambdas and computational work, `StepFunctions` to hold description of the state-machine graph and finally - `resources` where AWS Batch setup is defined.

## Next steps

- [ ] Add AWS Batch dir with StepFunction simple example
