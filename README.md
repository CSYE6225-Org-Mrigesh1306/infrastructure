# Assignment-3 : Infrastructure As Code using CloudFormation

### To Create VPC, Subnets, Internet Gateways & Route Table using CloudFormation on AWS


**Configure AWS profile and Region on AWS-CLI**

- export AWS_PROFILE=demo
- export AWS_REGION=us-east-1

**Create  Stack using Parameters**
- aws cloudformation create-stack --stack-name csye6225-Vpc --template-body file:///Users/mrigesh/Desktop/Cloud_Computing/CloudFormation/csye6225-infra.yml --parameter ParameterKey=VpcCIDRBlock,ParameterValue="10.0.0.0/16" ParameterKey=PublicSubnet1CIDR,ParameterValue="10.0.0.0/24" ParameterKey=PublicSubnet2CIDR,ParameterValue="10.0.1.0/24" ParameterKey=PublicSubnet3CIDR,ParameterValue="10.0.2.0/24"

**View Stack**
- aws cloudformation describe-stacks

**Delete Stack**
- aws cloudformation delete-stack --stack-name csye6225-Vpc



