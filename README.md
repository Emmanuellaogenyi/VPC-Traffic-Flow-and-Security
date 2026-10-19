# VPC Traffic Flow and Security

**Project Link:** [View Project](https://nextwork.ai/projects/fe5ed473-5874-57e1-a58f-d9b3d652330c)

**Author:** Emmanuella Ogenyi  
**Email:** emmanuella.ogenyi@gmail.com

---

![Image](https://nextwork.ai/lively_yellow_swift_lemon_balm/uploads/aws-networks-security_92b0b0b4)

## Introducing Today's Project!

### What is Amazon VPC?

 VPC is like your own private section of the AWS network, where you control the flow of network traffic in and out of the AWS resources. It is used for network isolation, custom networking, and hybrid cloud connectivity subnet isolation.

### How I used Amazon VPC in this project

i used Amazon VPC to create route tables, security group and network ACL (Network Acess Control List ).

### One thing I didn't expect in this project was...

I didn't expect it to be so understandable

### This project took me...

45 minutes

## Route tables

Route tables are like the GPS that directs traffic within my VPC in the right direction.

Route tables are necessary to make a subnet public because subnets require a route to an internet gateway to be considered public. A route table is the only way to establish this connection.

![Image](https://nextwork.ai/lively_yellow_swift_lemon_balm/uploads/aws-networks-security_0a07b191)

## Route destination and target

Routes are defined by their destination and target, which means the destination is the range of IP addresses that traffic in my VPC is trying to reach, and the target is the road path that the traffic will use to get to their destination.

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of 0.0.0.0/0 and a target of my nextwork IG (Internet gateway).

![Image](https://nextwork.ai/lively_yellow_swift_lemon_balm/uploads/aws-networks-security_0a07b191)

## Security groups

a security group is a security checkpoint that monitors both inbound and outbound traffic at the resource level.

### Inbound vs Outbound rules

Inbound rules control the data that can enter the resources in your security group. I configured an inbound rule that allows all inbound HTTP traffic.

 outbound rules control that data that your resources can send out.By default, my security group's outbound rule will allow all outbound traffic.

![Image](https://nextwork.ai/lively_yellow_swift_lemon_balm/uploads/aws-networks-security_92b0b0b4)

## Network ACLs

Network ACLs are used to set broad traffic rules that apply to an entire subnet level.

### Security groups vs. network ACLs

The difference between a security group and a network ACL is that a security group secures my network at the resource level while a network ACL secures my network at the subnet level.

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound rules is set to allow all incoming traffic.
By default, a network ACL's outbound rules is set to allow all outgoing traffic.

In contrast, a custom ACL’s inbound and outbound rules are automatically set to deny all incoming/outgoing traffic.

![Image](https://nextwork.ai/lively_yellow_swift_lemon_balm/uploads/aws-networks-security_4faeb056)

## Tracking VPC Resources

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/fe5ed473-5874-57e1-a58f-d9b3d652330c)*
