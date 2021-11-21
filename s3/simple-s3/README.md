
# SimpleS3

## Description
Creates a simple, no frills S3 Bucket. Probably not even useful. 


## Commands


Validate the template:

```bash
aws cloudformation validate-template --template-body file://template.yaml | jq
```

List the stacks:

```bash
aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE | jq
```

Delete the stack:

```bash
aws cloudformation delete-stack --stack-name simple-s3
```
