# Unit 5: Networking

## Amazon Virtual Private Cloud (VPC)

Helps you provision a private network on the cloud where you can provision whatever resources you want.

- **Public Resources**
- **Private Resources**

### Subnets

- Used to organize your resources into privately or publicly accessible groups
- Resources are placed into separate subnets — chunks of IP addresses — to make management easier
- Subnets allow you to control access to gateways

## Connecting to Your VPC

- **Internet Gateway**: Required to allow traffic to go into and out of your VPC
- **Virtual Private Gateway**: Allows protected internet traffic to enter the VPC
- **Virtual Private Network (VPN)**: Encrypts your internet traffic and protects it from anyone monitoring it
- **AWS Direct Connect**: A private connection from your data center to AWS

### Four Main Ways to Connect to the AWS Cloud

| Method | Description |
|---|---|
| **AWS Client VPN** | Connects remote workers and on-premises networks to the cloud; elastic and fully managed |
| **AWS Site-to-Site VPN** | Secure connection between your data center/branch offices and your AWS Cloud resources |
| **AWS PrivateLink** | Allows you to connect to resources from other cloud providers |
| **AWS Direct Connect** | Dedicated private connection between your network and your VPC in the AWS Cloud |

### Additional Gateway Services

- AWS Transit Gateway
- NAT Gateway
- Amazon API Gateway

## Subnet-Level Traffic Control

- **Network Access Control List (NACL)**: Every packet trying to enter the subnet gets checked against the NACL
- **Security Groups**: When multiple EC2 instances live within a subnet, you can apply a security group per instance to block certain traffic
  - By default, security groups let all outbound traffic go out
  - Security groups are **stateful** (retain some memory of connections)
  - Network ACLs are **stateless** (check all traffic every time, no memory)

## Global Networking

- **Amazon Route 53**: DNS service
  - Supports several routing policies, including latency-based routing, geolocation DNS, and weighted round robin
- **Amazon CloudFront**: CDN
- **AWS Global Accelerator**: A private global network that directs traffic more quickly

## Global Architectures