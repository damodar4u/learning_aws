s3
- cross account access with IAM user
- AWS - Implementing Cross Account Role Access
- AWS S3 Cross Region Replication
- AWS - S3 & CLI - Bucket Policy Demo for Cross-account access with IAM user



cross account access with IAM user


Use Aws policy generator

(effect, principal, servic, Action, ARN) , copy from policy generator and paste it in bucket policy.

aws configure (access key, secret access key) for a user

aws s3 ls s3://a1_bucket<from different account>

aws s3 cp s3://a1_bucket<from different account>/1.txt s3://a2_bucket<to_bucket_in_my_account>/ --dryrun


![Alt text](learning_aws/Cross_Account_s3.PNG?raw=true "Cross_Account_s3")


