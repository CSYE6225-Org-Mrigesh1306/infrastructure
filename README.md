# Assignment-10 :Secure Application Endpoints
 

## Encrypted EBS Volumes
* All EC2 instances must now be launched with encrypted EBS volumes.
* EBS volumes must be encrypted with Customer managed key created as part of your CloudFormation template.

## Encrypted RDS Instances
* RDS instances launched should be encrypted with (a separate) Customer managed key created as part of your CloudFormation template. The encryption key must not be shared with other resources.

## Command to import Certificate
* aws acm import-certificate --certificate fileb://demo_mrigeshdasgupta_me.crt --certificate-chain fileb://demo_mrigeshdasgupta_me.ca-bundle --private-key fileb://demo.pem --profile=demo

**Configure AWS profile and Region on AWS-CLI**

- export AWS_PROFILE=demo
- export AWS_REGION=us-east-1

**Create  Stack using Parameters**
- aws cloudformation create-stack --stack-name demo-stack --template-body file:///Users/mrigesh/Desktop/Cloud_Computing/infrastructure/infrastructure/csye6225-infra.yml --parameter ParameterKey=AMIImage,ParameterValue=ami-0#######  ParameterKey=ProfileName,ParameterValue=demo ParameterKey=DomainName,ParameterValue=demo.mrigeshdasgupta.me.  ParameterKey=accesskey,ParameterValue=AKIASPQXE######### ParameterKey=secretkey,ParameterValue=VREmPxC9QnS9FdW############ --capabilities CAPABILITY_NAMED_IAM

**View Stack**
- aws cloudformation describe-stacks

**Delete Stack**
- aws cloudformation delete-stack --stack-name demo-stack




