**aws-packer-basic**
===================


This is a simple packer file that take the latest Amazon Linux AMI and then performs some simple functions to get it updated and adds a few useful tools

----------


Contents
-------------

The packer file performs the following tasks

 - Selects the latest Amazon Linux AMI with the following characteristics
	 - HVM Virtualisation type
	 - EBS
	 - GP2
	 - Region = eu-west-2 (london)
 - sets ssh user name to ***ec2-user***
 - Performs a **yum update** to get the latest updates
 - Upgrades the **AWS CLI tool**
 - Installs **Git**
 - Downloads the **Amazon CloudWatch monitoring** scripts 
 - unzips CloudWatch scripts to /opt and cleans up
 - Installs **Ansible** via pip
 - Installs **AWS CloudWatch Logs Agent**
