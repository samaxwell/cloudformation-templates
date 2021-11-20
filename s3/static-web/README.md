
# Static Web 

## Description
Creates an S3 bucket for serving static web pages


## Commands


Validate the template:
```cli
aws cloudformation validate-template --template-body file://template.yaml | jq
```

Submit the template:
```cli
aws cloudformation deploy --template-file template.yaml --stack-name static-web
```

List the stacks:
```cli
aws cloudformation list-stacks --stack-status-filter CREATE_COMPLETE | jq
```

Get stack outputs:
```cli
aws cloudformation describe-stacks --stack-name static-web --query "Stacks[0].Outputs" | jq
```

Get stack resources (i.e. the s3 bucket name)
```cli
aws cloudformation describe-stack-resources --stack-name static-web | jq
```

Delete the stack:
```cli
aws cloudformation delete-stack --stack-name static-web
```
