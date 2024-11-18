# Elastic Cloud Computing (EC2)

It allows users to launch run and manage virtual servers which is also known as instances. This instances are customizable for example: CPU, Memory, Storage, Operating System, 

## Key features of EC2

* **Pay as you go** you only pay for the instance that you use. It is totaly based on your usage
* **Scalability** instances can be scaled up and down based on your requirement after launching an instance
* **Secure** It provides the secure access for instance by key pairs and security groups

## Overview of AMI
Amazon machine image it is a template that provides software configurations like operating systems and pre installed applications in an OS

## Instance Types
Instance types are predefined virtual servers which has CPU, storage, memory, and networking. Based on the requirement we can choose the instance type
for example:
* General purpose (starts with T)
* Compute Optimized (starts with C)
* Memory Optimized (starts with R)
* Storage Optimized (starts with I)
 
## Status Checks of EC2 Instance
Status checks will automatically checks the health of instances there are 2 types: 1. System status check 2. Instance status Check
* System status check: it checks the instance hardware like power and network if there is any failure then AWS will migrate the instance
* Instance status check: it checks the instance software like operating system whether the OS is responding or not

## Instance state
It will state the current state of the instance by which we can find out whether the instance is running, stoped, reboting or Terminated.\
Types of States:
* Pending: once you launch the instance it will take some time to start running
* Running: the instance is ready to perform actions on it
* Stopping: the instance is shutting down
* Stopped: the instance is stopped can be start
* Terminating: the instance is about to be deleted perminently
* Terminated: the instance is deleted perminently
* Rebooting: the instance is restarting
* Start: it will start the stopped instance
* Hibernate: it will pause the instance which means the data in memory will not be lost

## Reserved Instance
it is a feature that allows you to reserve instance for fixed period so that you will charge less compared to on-demand instance.

