
# Static Web 

## Description
Creates an S3 bucket for serving static web pages


## Commands


Validate the template:
- `aws cloudformation validate-template --template-body file://template.yaml | jq`

Submit the template:
- `aws cloudformation deploy --template-file template.yaml --stack-name static-web`

List the stacks:
- `aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE | jq`

Get stack outputs:
- `aws cloudformation describe-stacks --stack-name static-web --query "Stacks[0].Outputs" | jq`

Get stack resources (i.e. the s3 bucket name)
- `aws cloudformation describe-stack-resources --stack-name static-web | jq`


Delete the stack:
- `aws cloudformation delete-stack --stack-name static-web`