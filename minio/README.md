### Create access key
http://localhost:9001/access-keys

### Add credentials
https://aws.amazon.com/blogs/developer/new-improved-flexibility-when-configuring-endpoint-urls-with-the-aws-sdks-and-tools/
~/.aws/credentials
```
[minio]
aws_access_key_id=
aws_secret_access_key=
```
~/.aws/config
```
[profile minio]
services=local-services

[services local-services]
s3 =
  endpoint_url=http://localhost:9000
```

### Run AWS Cli
https://min.io/docs/minio/linux/integrations/aws-cli-with-minio.html
```bash
AWS_PROFILE=minio aws s3 ls
AWS_PROFILE=minio aws s3 ls s3://test1
AWS_PROFILE=minio aws s3 mb s3://newbucket
```