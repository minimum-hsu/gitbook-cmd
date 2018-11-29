---
tags:
  - aws
  - cloudwatch
  - awscli
---

# Delete CloudWatch Log Streams

AWS CloudWatch log group has retention attribute that retains log data for the specified period, but AWS do not delete streams from group. The following scripts use AWS CLI:

Delete all streams in the group:

```bash
export AWS_ACCESS_KEY_ID=<your access key>
export AWS_SECRET_ACCESS_KEY=<your secret access key>
export AWS_DEFAULT_REGION=<your region>
export GROUP=<your log group>
aws --output text logs describe-log-streams --log-group-name $GROUP --query logStreams[].logStreamName | xargs -n1 | xargs -I '{}' bash -c "aws logs delete-log-stream --log-group-name $GROUP --log-stream-name '{}'"
```

Delete lambda log streams in the specified date:

```bash
export AWS_ACCESS_KEY_ID=<your access key>
export AWS_SECRET_ACCESS_KEY=<your secret access key>
export AWS_DEFAULT_REGION=<your region>
export GROUP=<your log group>
export PREFIX=<specified date, ex: 2018/01/01>
aws --output text logs describe-log-streams --log-group-name $GROUP --log-stream-name-prefix $PREFIX --query logStreams[].logStreamName | xargs -n1 | xargs -I '{}' bash -c "aws logs delete-log-stream --log-group-name $GROUP --log-stream-name '{}'"
```

tags: aws, awscli, cloudwatch

