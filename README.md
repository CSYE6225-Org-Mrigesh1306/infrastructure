# Assignment-3 : Infrastructure As Code using CloudFormation

### To Create VPC, Subnets, Internet Gateways & Route Table using CloudFormation on AWS


**Configure AWS profile and Region on AWS-CLI**

- export AWS_PROFILE=demo
- export AWS_REGION=us-east-1

**Create  Stack**
- aws cloudformation create-stack --stack-name csye6225-Vpc --template-body file:///Users/mrigesh/Desktop/Demo/csye6225-infra.yml

**View Stack**
- aws cloudformation describe-stacks

**Delete Stack**
- aws cloudformation delete-stack --stack-name csye6225-Vpc



