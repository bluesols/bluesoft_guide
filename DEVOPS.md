# DevOps Process
This document contains the devops process for the different cloud platforms, technologies and guides to setup `Production`, `Staging` and `Development`  environment. 
## AWS
### IaC
1. We will be using AWS Cloudformation to setup the infrastructre on AWS.
2. Each each cloudformation stack will must have `Project` and `Env` parameters.
3. All the resources must be tagged with `Project` and `Env` parameters.
4. For security groups, IAM profiles or any resource that can be shared, outputs should be declared to use in another stack.
5. Use intrinsic functions to keep the stack easily editable.
6. Never hardcode the imports for IAM roles, security groups.
### AWS CLI install
To setup the aws profile for your local environment perform following steps.

1. Install aws cli
- For Ubuntu run following command in terminal
```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```
- For Windows open powershell as admin and run following command
```powershell
msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi
```
  
2. Confirm installation using following command
```bash
aws --version
```
3. To Create aws profile run following with the name of the AWS profile you want to set as the default:
```bash
aws configure --profile <ProfileName> #Example: aws configure --profile jungle-dev
```
You will be prompted to enter the following information:
- AWS Access Key ID
- AWS Secret Access Key
- Default region name (Ask devops person about the region or set us-east-1_
- Default output format (You can leave this as json)
Enter your Access Key ID and Secret Access Key when prompted.

4. To test run following command
```bash
aws s3 ls --profile <ProfileName>
```
It will list the current buckets if you're provided with s3 access.
