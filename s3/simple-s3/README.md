
# SimpleS3

## Description
Creates a simple, no frills S3 Bucket. Probably not even useful. 


## Commands


Validate the template:
- `aws cloudformation validate-template --template-body file://template.yaml | jq`

List the stacks:
- `aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE | jq`

Delete the stack:
- `aws cloudformation delete-stack --stack-name simple-s3`