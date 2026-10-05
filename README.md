<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Testing VPC Connectivity

**Project Link:** [View Project](https://nextwork.ai/projects/da091986-ef01-5973-a070-b15e174f59d8)

**Author:** Ahmed Umar Rehman  
**Email:** ahmedumar475@gmail.com

---

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/da091986-ef01-5973-a070-b15e174f59d8_8ee57662)

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a logically isolated virtual network in AWS, and it is useful because it lets you securely control your resources, networking, and traffic.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to test connectivity between my EC2 instances and the internet.


### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how many networking components work together to enable and secure connectivity in a VPC.

### This project took me...

This project took me around 1.5 hours 

## Connecting to an EC2 Instance

Connectivity means the ability of two or more devices or resources to communicate with each other over a network.

My first connectivity test was whether I could connect to **my public server from my local computer using SSH.**


![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/da091986-ef01-5973-a070-b15e174f59d8_88727bef)

## EC2 Instance Connect

I connected to my EC2 instance using EC2 Instance Connect, which is a way to securely access an EC2 instance directly through the AWS Management Console using SSH.

My first attempt at getting direct access to my public server resulted in an error, because its security group did not allow inbound SSH traffic, which EC2 Instance Connect requires.

I fixed this error by adding an inbound SSH rule to my public server's security group and allowing SSH traffic from Anywhere-IPv4.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/da091986-ef01-5973-a070-b15e174f59d8_1cbb1b88)

## Connectivity Between Servers

Ping is a network command used to test whether one device can reach another; I used ping to test the connectivity between my public and private EC2 instances.

The ping command I ran was `ping <private EC2 instance's private IP address>`.


The first ping returned Request timed out. This meant the private server was not responding to the ping, indicating that ICMP traffic was being blocked or not allowed.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/da091986-ef01-5973-a070-b15e174f59d8_defghijk)

## Troubleshooting Connectivity

I troubleshooted this by checking the private server's security group and allowing ICMP traffic from the public server's security group.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/da091986-ef01-5973-a070-b15e174f59d8_4a9e8014)

## Connectivity to the Internet

cURL is a command-line tool used to send requests to websites or servers and receive data from them.

I used cURL to test the connectivity between my EC2 instance and the internet.

### Ping vs Curl

Ping and cURL are different because ping tests whether a device is reachable, while cURL tests whether you can connect to a website/server and retrieve data.

## Connectivity to the Internet

I ran the cURL command, which returned the HTML content of the NextWork webpage.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/da091986-ef01-5973-a070-b15e174f59d8_8ee57662)

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/da091986-ef01-5973-a070-b15e174f59d8)*
