# Unit 2 Notes

## Amazon Elastic Cloud (EC2)

- Offers flexibility in pricing
- They are Virtual Machines that share one host machine
- **Multitenancy:** Sharing underlying hardware between virtual machines
- When you provision custom Amazon EC2 configurations (Windows, Linux, Business apps, web apps, databases, third party software)
- EC2 Instances are resizable
- **Vertical Scaling:** giving an instance more memory and CPU
- Can control the networking aspect of EC2 about what types of network requests come through and whether it's public or private.
- AWS offers this as a Compute As a Service Model

### To launch an instance

1. **Step 1:** select an Amazon Machine Image (AMI) to define OS and underlying hardware resources
2. **Step 2:** Connect to the instance over the network using SSH for linux instances. Remote Desktop Protocol (RDP) for windows instances, or use an AWS service like AWS Systems Manager
3. **Step 3:** Use the instance to run commands, install software, add storage etc

## Types of EC2 Instance Types

### Instance Families

- **General Purpose:** good balance of resources, diverse workloads, web servers, code repos
- **Compute Optimized:** computer intensive tasks, HPC, gaming
- **Memory optimized:** fast performance for workloads that process large data sets
- **Accelerated computing:** performs calculations and functions very efficiently ( Use GPUs)
- **Storage Optimized:** for workloads dependent on locally stored data

## How to provision Resources

- Everything is an API Call
- **API:** application program interface | predefined behaviors to interact with AWS services

### Interacting with AWS services through

- **Management console (browser based):** set up test environments, aws bills, view monitoring, first time users
- **Command Line Interface:** Make API calls using the terminal on your machine
- **Software development kit:** Using AWS through your code

## Amazon Machine Image

- pre-built virtual machine images that have the basic components for what is needed to start an instance
- Include the OS, storage set up, architecture type, permissions for launching.
- You can use the same AMi launch multiple EC2 Instances

## Amazon EC2 Pricing Types

- On-demand
- Savings Plan (lower prices but need to commit to 1 year or 3 year term)
- reserved instances (for very predictable workloads, gives discount options for ⅓ year terms)
- Spot Instnaces (up to 90% off but AWS can turn it off whenever)
- Dedicated Hosts (Solely for customer)

## Scaling EC2

- **Scalability:** ability to handle an increased load and long term capacity
- **Elasticity:** scale resources in response to real time demand
- EC2 provides auto scaling according to real time demand
- **Dynamic Scaling:** adjust sin real time to fluctuations in demand
- **Predictive scaling:** preemptively schedules the right number of instances based on anticipated demand
- Auto Scaling Group of EC2 instances that can scale in and out to meet your apps needs. They have 2 key settings: min, desired, and max capacity
- Amazon CloudWatch provides monitoring resources

## Elastic Load Balancing (ELB)

- Distributes network traffic
- Routing methods include Round Robin, least connections, IP Hash(client goes to same server every time), and LRT

## Messaging & Queuing

- Tightly Coupled architecture is risky
- **Amazon Simple Queue Service (SQS)**
  - Messages are payloads and stored within a SQS queue
- **Amazon Simple Notification Services (SNS)**

### Type of systems

- **Monolithic applications:** consist of multiple components that work together to transmit data; are tightly coupled; very risky
- **Microservices architecture:** loosely coupled; if one component fails others function normally
- **Amazon EventBridge:** serverless service that helps connect different parts of an application using events.
