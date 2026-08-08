# Unit 3: AWS Compute Services

## Serverless vs. Managed vs. Unmanaged

- **Serverless**: Can't see or access the underlying infrastructure
- **Unmanaged**: EC2
- **Managed**: ELB, SNS, SQS

## AWS Lambda

- A Lambda function runs on some kind of trigger
- Maximum duration is **15 minutes**
- Good for handling website requests; supports all programming languages
- AWS handles scaling and all server-side infrastructure
- User needs to provide:
  - Lambda function
  - Trigger
  - Runtime

## Containers

Packages the code, dependencies, configurations, and data needed for a program to run into a single unit. Since you can have many containers in a cluster, you need **orchestration** to manage them.

### AWS Container Services

| Service | Description |
|---|---|
| **ECS** (Elastic Container Service) | Streamlined and integrated; fully managed service, but you can still define parameters |
| **EKS** (Elastic Kubernetes Service) | Open-source platform; more complex, offers more control and flexibility; automates container deployment, scaling, and management |
| **ECR** (Elastic Container Registry) | Stores container images in an inventory |

### Hosting Options

- **EC2**: Full control but more management overhead
- **Fargate**: Serverless — AWS manages everything

## Other Compute Services

- **AWS Elastic Beanstalk**: A managed service for deploying and scaling web applications
- **AWS Batch**: A fully managed service for batch computing workloads; automatically schedules, manages, and scales resources for batch jobs
- **Amazon Lightsail**: A simplified AWS experience with virtual private servers (VPSs), storage, and networking — without the complexity of the full AWS management console
- **AWS Outposts**: A hybrid cloud service that extends AWS services to on-premises data centers