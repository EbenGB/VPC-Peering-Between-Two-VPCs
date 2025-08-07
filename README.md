# VPC Peering Between Two VPCs

## Description
This project demonstrates how to connect two separate AWS VPCs using VPC Peering. The setup allows private communication between resources in two VPCs across the same or different AWS regions.

## AWS Services Used
- Amazon VPC
- VPC Peering
- Route Tables
- Security Groups

## Instructions

### 1. Create Two VPCs
- VPC A CIDR block: 10.0.0.0/16
- VPC B CIDR block: 10.1.0.0/16

### 2. Create Subnets in Each VPC
- VPC A: Subnet 10.0.1.0/24
- VPC B: Subnet 10.1.1.0/24

### 3. Launch EC2 Instances in Both VPCs
- Launch EC2 A in VPC A subnet
- Launch EC2 B in VPC B subnet

### 4. Create a VPC Peering Connection
- Initiate peering from VPC A to VPC B
- Accept the request from VPC B

### 5. Update Route Tables
- In VPC A route table: Add route to 10.1.0.0/16 via peering connection
- In VPC B route table: Add route to 10.0.0.0/16 via peering connection

### 6. Modify Security Groups
- Allow traffic between the EC2 instances across the two VPCs (e.g., ICMP or SSH)

### 7. Test the Connection
- Ping from EC2 A to EC2 B or use SSH (ensure security groups allow it)

## Diagram
See the architecture diagram included in this project.

## Author
Ebenezer Gbormittah
