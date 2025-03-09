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

## Create EC2 instances in the subnets
For instances created in the private subnets, we will need a NAT gateway so they can communicate to the Internet. NAT gateways always go in public subnets

For the instances in the private subnets to access this natgw, they're gonna need a route to the natgw which we must add to the private route table