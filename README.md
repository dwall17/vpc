# Let's make a VPC

## Create the CIDR block
VPC Name: my-vpc
CIDR block: 10.0.0.0/16

## Create subnets
Name: public-1a
Subnet: 10.0.1.0/24
Availability Zone: us-east-1a

Name: public-1b
Subnet: 10.0.2.0/24
Availability Zone: us-east-1b

Name: private-1a
Subnet: 10.0.3.0/24
Availability Zone: us-east-1a

Name: private-1a
Subnet: 10.0.4.0/24
Availability Zone: us-east-1b

## Create private route table
Name: private-rt
VPC: my-vpc
Subnet assocations: private-1a, private-1b

## Create Internet Gateway
Name: my-igw
VPC: my-vpc
