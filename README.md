# EKS / Kubernetes - 101 in AWS

This is just for educational purposes, just barely scratch the surface using eksctl will make your life easier specially setting up the EKS cluster otherwise
you are going to have an excruciating pain on setting it up which is a good thing if you want to know EKS better, you had been warned!!

I'm going to update this repository from time to time

## TODO

PODS to outside world integration like RDS
PODS persistent volumes best practices
CLI cheat sheets

## Pre-requisite and assumption

Contact AWS support and activate your cloudshell or setup your own environment to have kubectl / helm and eksctl install on your computer

You need to configure your aws cli tools to with your Access and Secret key otherwise the userland tools won't be able to contact AWS this is important
if you use cloudshell you don't have to do this

The EKS cluster will be named "lab" and will be place in ap-southeast-1 (Singapore) and the nodegroup will be called "g1"

If you need help just give me a shout!

```python
# Your Access Key and Secret is only available after you enable and activate your account in AWS, it takes 24 hours so be patient
# In your operating system terminal 'aws configure'

AWS Access Key ID [None]: YOUR_ACCESS_KEY_ID
AWS Secret Access Key [None]: YOUR_SECRET_ACCESS_KEY
Default region name [None]: ap-southeast-1
Default output format [None]: json

```
Always terminate your AWS eks after use this is a 4 worker nodes so expect a bill please setup your AWS Budget to a decent amount like 5 to 10 USD
