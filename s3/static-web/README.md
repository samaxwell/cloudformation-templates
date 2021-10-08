
# Static Web 

## Description
Creates an S3 bucket for serving static web pages


## Commands


Validate the template:
- `aws cloudformation validate-template --template-body file://template.yaml | jq`

List the stacks:
- `aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE | jq`

Delete the stack:
- `aws cloudformation delete-stack --stack-name static-web`