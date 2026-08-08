# AWS Cloud Practitioner — Unit 1

## Cloud Computing

**Definition:** On-demand delivery of IT resources over the internet with pay-as-you-go pricing.

## Cloud Deployment Models

| Model | Description |
| --- | --- |
| **Cloud** | Ability to migrate existing resources to the cloud, design and build new apps, or both. |
| **On-premises** | Traditional IT infrastructure where companies own their hardware and boost efficiency using techniques like virtualization. Still difficult to scale and lacks the benefits of the cloud. Companies may choose this for dedicated resources or lower latency. |
| **Hybrid** | A mix of both. For example, on-premises for regulated legacy applications and cloud services for advanced data processing and analytics. |

## Benefits of the Cloud

- **Variable expenses** — Paying only for actual usage creates more financial flexibility.
- **Economies of scale** — AWS's large global infrastructure lets it provide resources at lower costs, making them accessible to companies of any size.
- **Scalability** — No need to guess how much compute you need. AWS automatically provisions more resources based on real-time demand.
- **Quick & easy** — Companies can deploy apps and services quickly, keeping operations efficient.
- **Removes need for data centers** — No need to maintain your own physical data centers.
- **Global reach** — Deploy applications and services across the globe without setting up infrastructure abroad.

## Intro to AWS Global Infrastructure

- **AWS Regions** — Locations around the world containing groups of data centers.
- **Availability Zones (AZs)** — Each group of data centers is an availability zone. Every AWS Region has a **minimum of 3** separate availability zones within a geographic area.
- **Resilience** — If one AZ goes down, customers can still operate without interruption because other zones remain available.

## AWS Shared Responsibility Model

**Security *of* the cloud (AWS) vs. security *in* the cloud (customer).**

| Responsibility | Owner |
| --- | --- |
| Customer data; client-side data encryption | **Customer** |
| Software for compute, storage, database, networking; hardware; AWS global infrastructure | **AWS** |
| Server-side encryption; network traffic protection; platform & application management; OS, network, and firewall configuration | **Customer or AWS** (depends on the service) |
