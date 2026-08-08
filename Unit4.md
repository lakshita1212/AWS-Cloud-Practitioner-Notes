# Unit 4: AWS Global Infrastructure & IaC

## Regions

Each region is isolated from every other region. Data cannot move between regions unless permission is given.

### Considerations When Choosing a Region

- **Compliance**: Geographic compliance laws may force you to pick a specific region
- **Proximity**: Distance to your customer base affects latency
- **Feature Availability**: The closest region may not have all the features you need
- **Pricing**: Some locations are more cost-effective to operate in

## Planning for Long-Term Stability

- **Multi-AZ resources**: Deploying cloud resources across multiple regions and multiple availability zones (AZs)
  - **High Availability**: If one region/AZ has an issue, switch to another
  - **Agility / Latency**: Serve customers quickly by being closer to them

## Amazon CloudFront

A content delivery network (CDN) designed to provide content to users as fast as possible using **edge locations**.

- **Edge Locations**: AWS's global edge network, placed in high-population areas (e.g., Atlanta, Georgia; Shanghai, China) to provide low latency to users
  - Separate from regions
  - Host other AWS accelerators
  - Support Amazon Route 53 (DNS)
  - Support CloudFront for content delivery

- **AWS Outposts**: High-speed; allows you to run AWS services on-premises

## Infrastructure as Code (IaC)

A blueprint of your architecture that lets you deploy the same setup multiple times.

### AWS CloudFormation

- Lets you create text-based documents called **CloudFormation templates**
- CloudFormation parses the template and deploys it
- Deploying the same template across multiple regions produces identical results and reduces human error