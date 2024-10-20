# EKS / Kubernetes - 101 in AWS

This is just for educational purposes, just barely scratch the surface using eksctl will make your life easier specially setting up the EKS cluster otherwise
you are going to have an excruciating pain on setting it up which is a good thing if you want to know EKS better, you had been warned!!

I'm going to update this repository from time to time

## Reminder please remove AWS config on your account this cost a lot 
aws configservice delete-configuration-recorder --configuration-recorder-name default --region ap-southeast-1

## BOOTSTRAPING

clone this repository run both shell scripts located at scripts folder then execute provision script and supplied appropriate parameters match to your environment</br></br>
[cloudshell-user@ip-10-132-11-60]$ git clone https://github.com/rpchan44/learn-aws-eks.git </br>
[cloudshell-user@ip-10-132-11-60]$ cd learn-aws-eks </br>
[cloudshell-user@ip-10-132-11-60 learn-aws-eks]$ cd scripts/</br>
[cloudshell-user@ip-10-132-11-60 scripts]$ sh get_eksctl.sh </br>
eksctl_Linux_amd64.tar.gz: OK </br>
[cloudshell-user@ip-10-132-11-60 scripts]$ sh get_helm.sh </br>
Downloading https://get.helm.sh/helm-v3.16.2-linux-amd64.tar.gz </br>
Verifying checksum... Done.</br>
Preparing to install helm into ..</br>
helm installed into ../helm </br>
[cloudshell-user@ip-10-132-11-60 scripts]$ cd .. </br>
[cloudshell-user@ip-10-132-11-60 learn-aws-eks]$ chmod +x provision </br>
[cloudshell-user@ip-10-132-11-60 learn-aws-eks]$ ./provision </br>
<b>Error!: usage ./provision cluster_name aws_account region_name num_worker_nodes</b></br>
[cloudshell-user@ip-10-132-11-60 learn-aws-eks]$

## TODO

PODS to outside world integration like RDS </br>
PODS persistent volumes with efs </br>
CLI cheat sheets

`Resizing nodegroup if you need more capacity`</br>
<b>./eksctl --cluster lab scale nodegroup --name g1 --nodes-max 6 --nodes 4

## RESEARCH and Validation phase
Installing efs-csi driver using helm</br>

## Pre-requisite and assumption

Contact AWS support and activate your cloudshell or setup your own environment to have kubectl / helm and eksctl install on your computer

You need to configure your aws cli tools together with your Access and Secret key otherwise the userland tools won't be work this is important if you use cloudshell you don't have to do this

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

![Screenshot 1](https://github.com/rpchan44/learn-aws-eks/blob/master/images/1.png)
![Screenshot 2](https://github.com/rpchan44/learn-aws-eks/blob/master/images/2.PNG)
![Screenshot 3](https://github.com/rpchan44/learn-aws-eks/blob/master/images/3.PNG)
