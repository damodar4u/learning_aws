<<<<<<< HEAD
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


copy everything recursively

aws s3 cp s3://a1_bucket<from different account>/1.txt s3://a2_bucket<to_bucket_in_my_account>/ --recursive --dryrun 



![Alt text](learning_aws/Cross_Account_s3.PNG?raw=true "Cross_Account_s3")


=======
s3
- cross account access with IAM user
- AWS - Implementing Cross Account Role Access
- AWS S3 Cross Region Replication
- AWS - S3 & CLI - Bucket Policy Demo for Cross-account access with IAM user



cross account access with IAM user


Use Aws policy generator

(effect, principal, servic, Action, ARN) , copy from policy generator and paste it in bucket policy.

cross account access you should specify the 12 digit account ID. 


aws configure (access key, secret access key) for a user

aws s3 ls s3://a1_bucket<from different account>

aws s3 cp s3://a1_bucket<from different account>/1.txt s3://a2_bucket<to_bucket_in_my_account>/ --dryrun


copy everything recursively

aws s3 cp s3://a1_bucket<from different account>/1.txt s3://a2_bucket<to_bucket_in_my_account>/ --recursive --dryrun 



![Alt text](Cross_Account_s3.JPG?raw=true "Cross_Account_s3")



Access S3 buckets from EC2 instances with IAM role

1) create a role with s3 full access
2) Launch an instance with role
3) access s3 bucket with aws cli commands



advantage with role we will not be providing any credentials to access s3 bucket


mount S3 on EC2 Instance

1) create an ec2 instance with its own user and download its keypair
2) create a new user from IAm with full access to s3 policy attached to the user and note down both secret key and secret access key
3) create a bucket
4) install s3fs from github
5) create mount using s3fs by using the credentials from newly created user copied to /etc/passwd_fsuser
6) run s3fs command to mount the bucket to created directory


install s3fs 


Access 
