# DevOps Process
This document contains the devops process for the different cloud platforms, technologies and guides to setup `Production`, `Staging` and `Development`  environment. 
## AWS
### IaC
1. We will be using AWS Cloudformation to setup the infrastructre on AWS.
2. Each each cloudformation stack will must have `Project` and `Env` parameters.
3. All the resources must be tagged with `Project` and `Env` parameters.
4. For security groups, IAM profiles outputs should be declared to use in another stack.


