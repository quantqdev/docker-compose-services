### Create access key
http://localhost:9001/access-keys

### Add credentials
```
[minio]
aws_access_key_id=
aws_secret_access_key=
```

### Run AWS Cli
https://min.io/docs/minio/linux/integrations/aws-cli-with-minio.html
```bash
AWS_PROFILE=minio aws --endpoint-url http://localhost:9000 s3 ls
AWS_PROFILE=minio aws --endpoint-url http://localhost:9000 s3 ls s3://test1
AWS_PROFILE=minio aws --endpoint-url http://localhost:9000 s3 mb s3://newbucket
```