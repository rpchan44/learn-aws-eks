# EKS / Kubernetes - 101 in AWS

This is just for educational purposes, just barely scratch the surface

## Pre-requisite and assumption

Contact AWS support and activate your cloudshell or setup your own environment to have kubectl / helm and eksctl install on your computer

You need to configure your aws cli tools to with your Access and Secret key otherwise the userland tools won't be able to contact AWS this is important
if you use cloudshell you don't have to do this

```python
# Your Access Key and Secret is only available after you enable and activate your account in AWS, it takes 24 hours so be patient
# In your operating system terminal 'aws configure'

AWS Access Key ID [None]: YOUR_ACCESS_KEY_ID
AWS Secret Access Key [None]: YOUR_SECRET_ACCESS_KEY
Default region name [None]: ap-southeast-1
Default output format [None]: json

```
always terminate your AWS eks after use this is a 4 worker nodes so expect a bill please setup your AWS Budget to a decent amount like 5 to 10 USD
