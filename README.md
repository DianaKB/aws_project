# aws_project

### Step 1 - Create bucket on the AWS
(The main goal is to create a bucket for static website hosting) 

1. Select region and disable Block all public access/
2. Setting Properties (enable website hosting) and Permissions (for work with bucket, like add files, delete, read)
3. Add an AMI user for deployment from GitHub (set Permissions to get access keys).

### Step 2 - Configure GitHub
(The primary objective is to set up a repository with workflows for deployment on AWS.)

1. Enter the Access Key ID value and the Secret Access Key in this GitHub 
Repository settings.
2. Create a Workflow.
The main thing is that we have enough permissions in the bucket to deploy (Step 1.2).
Now we can check the website S3 Site http://diawsproject.ua.s3-website.eu-north-1.amazonaws.com/.

### Step 3 - Setup DNS

1. Register a domain on AWS Route 53 (create a Hosted zone.)
2. Set up the same name for the zone as bucket
3. Add alias for A record, where value is our bucket
