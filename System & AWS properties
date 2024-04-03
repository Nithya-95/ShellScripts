#!/bin/bash

###############################################################################################################
#Author  : Nithya
#Version : V1
#Date    : 03-04-2024
#This is a sample script to list  both system & AWS account properties & append the output into a html file

################################################################################################################

set -x #debugmode
set -e #exit the script when there is an error
set -o pipefail

#diskspace
df -h


#memory
free

#CPU
nproc

#for all the above
#top

#process
ps -ef

#For specific process
ps -ef | grep amazon

# process ID of speific process
ps -ef | grep amazon | awk -F" " '{print $2}'

# list s3 buckets
aws s3 ls

# list IAM users
aws iam list-users

# list EC2 instances
aws ec2 describe-instances

# list Ec2 instance ID
aws ec2 describe-instances | jq '.Reservations[].Instances[].InstanceId'

# list lambda functions
aws lambda list-functions

echo  Sript is successful!
