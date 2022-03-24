# Assignment-6 :IAM Users, Roles & Policies

### To Create LoadBalancer, Autoscaling Application Stack & Route53 with Cloudformation


**Configure AWS profile and Region on AWS-CLI**

- export AWS_PROFILE=demo
- export AWS_REGION=us-east-1

**Create  Stack using Parameters**
- aws cloudformation create-stack --stack-name demo-stack --template-body file:///Users/mrigesh/Desktop/Cloud_Computing/infrastructure/infrastructure/csye6225-infra.yml --parameter ParameterKey=AMIImage,ParameterValue=ami-0#######  ParameterKey=ProfileName,ParameterValue=demo ParameterKey=DomainName,ParameterValue=demo.mrigeshdasgupta.me.  ParameterKey=accesskey,ParameterValue=AKIASPQXE######### ParameterKey=secretkey,ParameterValue=VREmPxC9QnS9FdW############ --capabilities CAPABILITY_NAMED_IAM

**View Stack**
- aws cloudformation describe-stacks

**Delete Stack**
- aws cloudformation delete-stack --stack-name demo-stack

**Load Testing on WebServer**
- while true; do curl http://demo.mrigeshdasgupta.me/healthz/ ; done



