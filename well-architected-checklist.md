# AWS Well-Architected Framework

Provides guidance to help customers apply best practices in the design, delivery, and maintenance of AWS environments. 

**The Five Pillars of the Framework**

Incorporating these pillars into your architecture will help you produce stable and efficient systems. This will allow you to focus on the other aspects of design, such as functional requirements.
- Cost Optimization
- Reliability
- Operational Excellence
- Performance Efficiency
- Security

## [Cost Optimization](https://wa.aws.amazon.com/wat.pillar.costOptimization.en.html)

The Cost Optimization pillar includes the ability to run systems to deliver business value at the lowest price point.

  - The ability to avoid or eliminate unneeded cost or suboptimal resources.
  - There are four best practice areas and tools for cost optimization in the cloud:
  - Cost-Effective Resources – Cost Explorer, Amazon CloudWatch and Trusted Advisor, Amazon Aurora for RDS, AWS Direct Connect with Amazon CloudFront
  - Matching supply and demand – Auto Scaling
  - Expenditure Awareness –  AWS Cost Explorer, AWS Budgets
  - Optimizing Over Time – AWS News Blog and the What’s New section on the AWS website, AWS Trusted Advisor

Key AWS service:
- Cost Explorer

### Considerations

**COST 1: How do you implement cloud financial management?**

Implementing Cloud Financial Management enables organizations to realize business value and financial success as they optimize their cost and usage and scale on AWS.

**COST 2: How do you govern usage?**

Establish policies and mechanisms to ensure that appropriate costs are incurred while objectives are achieved. By employing a checks-and-balances approach, you can innovate without overspending.

**COST 3: How do you monitor usage and cost?**

Establish policies and procedures to monitor and appropriately allocate your costs. This allows you to measure and improve the cost efficiency of this workload.

**COST 4: How do you decommission resources?**

Implement change control and resource management from project inception to end-of-life. This ensures you shut down or terminate unused resources to reduce waste.

**COST 5: How do you evaluate cost when you select services?**

Amazon EC2, Amazon EBS, and Amazon S3 are building-block AWS services. Managed services, such as Amazon RDS and Amazon DynamoDB, are higher level, or application level, AWS services. By selecting the appropriate building blocks and managed services, you can optimize this workload for cost. For example, using managed services, you can reduce or remove much of your administrative and operational overhead, freeing you to work on applications and business-related activities.

**COST 6: How do you meet cost targets when you select resource type, size and number?**

Ensure that you choose the appropriate resource size and number of resources for the task at hand. You minimize waste by selecting the most cost effective type, size, and number

**COST 7: How do you use pricing models to reduce cost?**

Use the pricing model that is most appropriate for your resources to minimize expense.

**COST 8: How do you plan for data transfer charges?**

Ensure that you plan and monitor data transfer charges so that you can make architectural decisions to minimize costs. A small yet effective architectural change can drastically reduce your operational costs over time.

**COST 9: How do you manage demand, and supply resources?**

For a workload that has balanced spend and performance, ensure that everything you pay for is used and avoid significantly underutilizing instances. A skewed utilization metric in either direction has an adverse impact on your organization, in either operational costs (degraded performance due to overutilization), or wasted AWS expenditures (due to over-provisioning).

**COST 10: How do you evaluate new services?**

As AWS releases new services and features, it's a best practice to review your existing architectural decisions to ensure they continue to be the most cost effective.


## [Reliability](https://wa.aws.amazon.com/wat.pillar.reliability.en.html)

The Reliability pillar includes the ability of a workload to perform its intended function correctly and consistently when it’s expected to. this includes the ability to operate and test the workload through its total lifecycle. this paper provides in-depth, best practice guidance for implementing reliable workloads on AWS.

- The ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues.
- There are three best practice areas and tools for reliability in the cloud:
  - Foundations – IAM, Amazon VPC, AWS Trusted Advisor, AWS Shield
  - Change Management – AWS CloudTrail, AWS Config, Auto Scaling, Amazon CloudWatch
  - Failure Management – AWS CloudFormation, Amazon S3, AWS KMS, Amazon Glacier

Key AWS service:
- Amazon CloudWatch

### Considerations

**REL 1: How do you manage service quotas and constraints?**

For cloud-based workload architectures, there are service quotas (which are also referred to as service limits). These quotas exist to prevent accidentally provisioning more resources than you need and to limit request rates on API operations so as to protect services from abuse. There are also resource constraints, for example, the rate that you can push bits down a fiber-optic cable, or the amount of storage on a physical disk.

**REL 2: How do you plan your network topology?**

Workloads often exist in multiple environments. These include multiple cloud environments (both publicly accessible and private) and possibly your existing data center infrastructure. Plans must include network considerations such as intra- and inter-system connectivity, public IP address management, private IP address management, and domain name resolution.

**REL 3: How do you design your workload service architecture?**

Build highly scalable and reliable workloads using a service-oriented architecture (SOA) or a microservices architecture. Service-oriented architecture (SOA) is the practice of making software components reusable via service interfaces. Microservices architecture goes further to make components smaller and simpler.

**REL 4: How do you design interactions in a distributed system to prevent failures?**

Distributed systems rely on communications networks to interconnect components, such as servers or services. Your workload must operate reliably despite data loss or latency in these networks.

Components of the distributed system must operate in a way that does not negatively impact other components or the workload. These best practices prevent failures and improve mean time between failures (MTBF).

**REL 5: How do you design interactions in a distributed system to mitigate or withstand failures?**

Distributed systems rely on communications networks to interconnect components (such as servers or services). Your workload must operate reliably despite data loss or latency over these networks. Components of the distributed system must operate in a way that does not negatively impact other components or the workload. These best practices enable workloads to withstand stresses or failures, more quickly recover from them, and mitigate the impact of such impairments. The result is improved mean time to recovery (MTTR).

**REL 6: How do you monitor workload resources?**

Logs and metrics are powerful tools to gain insight into the health of your workload. You can configure your workload to monitor logs and metrics and send notifications when thresholds are crossed or significant events occur. Monitoring enables your workload to recognize when low-performance thresholds are crossed or failures occur, so it can recover automatically in response.

**REL 7: How do you design your workload to adapt to changes in demand?**

A scalable workload provides elasticity to add or remove resources automatically so that they closely match the current demand at any given point in time.

**REL 8: How do you implement change?**

Controlled changes are necessary to deploy new functionality, and to ensure that the workloads and the operating environment are running known software and can be patched or replaced in a predictable manner. If these changes are uncontrolled, then it makes it difficult to predict the effect of these changes, or to address issues that arise because of them.

**REL 9: How do you back up data?**

Back up data, applications, and configuration to meet your requirements for recovery time objectives (RTO) and recovery point objectives (RPO).

**REL 10: How do you use fault isolation to protect your workload?**

Fault isolated boundaries limit the effect of a failure within a workload to a limited number of components. Components outside of the boundary are unaffected by the failure. Using multiple fault isolated boundaries, you can limit the impact on your workload.

**REL 11: How do you design your workload to withstand component failures?**

Workloads with a requirement for high availability and low mean time to recovery (MTTR) must be architected for resiliency.

**REL 12: How do you test reliability?**

After you have designed your workload to be resilient to the stresses of production, testing is the only way to ensure that it will operate as designed, and deliver the resiliency you expect.

**REL 13: How do you plan for disaster recovery (DR)?**

Having backups and redundant workload components in place is the start of your DR strategy. RTO and RPO are your objectives for restoration of your workload. Set these based on business needs.

Implement a strategy to meet these objectives, considering locations and function of workload resources and data. The probability of disruption and cost of recovery are also key factors that help to inform the business value of providing disaster recovery for a workload.


## [Operational Excellence](https://wa.aws.amazon.com/wat.pillar.operationalExcellence.en.html)
The Operational Excellence pillar includes the ability to support development and run workloads effectively, gain insight into their operations, and to continuously improve supporting processes and procedures to deliver business value.

- The ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures.
- There are three best practice areas and tools for operational excellence in the cloud:
  - Prepare – AWS Config
  - Operate – Amazon CloudWatch
  - Evolve – Amazon Elasticsearch Service

Key AWS service:
- AWS CloudFormation for creating templates


### Considerations

**OPS 1: How do you determine what your priorities are?**

Everyone needs to understand their part in enabling business success. Have shared goals in order to set priorities for resources. This will maximize the benefits of your efforts.

**OPS 2: How do you structure your organization to support your business outcomes?**

Your teams must understand their part in achieving business outcomes. Teams need to understand their roles in the success of other teams, the role of other teams in their success, and have shared goals. Understanding responsibility, ownership, how decisions are made, and who has authority to make decisions will help focus efforts and maximize the benefits from your teams.

**OPS 3: How does your organizational culture support your business outcomes?**

Provide support for your team members so that they can be more effective in taking action and supporting your business outcome.

**OPS 4: How do you design your workload so that you can understand its state?**

Design your workload so that it provides the information necessary across all components (for example, metrics, logs, and traces) for you to understand its internal state. This enables you to provide effective responses when appropriate.

**OPS 5: How do you reduce defects, ease remediation, and improve flow into production?**

Adopt approaches that improve flow of changes into production, that enable refactoring, fast feedback on quality, and bug fixing. These accelerate beneficial changes entering production, limit issues deployed, and enable rapid identification and remediation of issues introduced through deployment activities.

**OPS 6: How do you mitigate deployment risks?**

Adopt approaches that provide fast feedback on quality and enable rapid recovery from changes that do not have desired outcomes. Using these practices mitigates the impact of issues introduced through the deployment of changes.

**OPS 7: How do you know that you are ready to support a workload?**

Evaluate the operational readiness of your workload, processes and procedures, and personnel to understand the operational risks related to your workload.

**OPS 8: How do you understand the health of your workload?**

Define, capture, and analyze workload metrics to gain visibility to workload events so that you can take appropriate action.

OPS 9: How do you understand the health of your operations?

Define, capture, and analyze operations metrics to gain visibility to operations events so that you can take appropriate action.

**OPS 10: How do you manage workload and operations events?**

Prepare and validate procedures for responding to events to minimize their disruption to your workload.

**OPS 11: How do you evolve operations?**

Dedicate time and resources for continuous incremental improvement to evolve the effectiveness and efficiency of your operations.


## [Performance Efficiency](https://wa.aws.amazon.com/wat.pillar.performance.en.html)

The Performance Efficiency pillar includes the ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.

- The ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.
- There are four best practice areas for performance efficiency in the cloud:
  - Selection – Auto Scaling for Compute, Amazon EBS and S3 for Storage, Amazon RDS and DynamoDB for Database, Route53, VPC, and AWS Direct Connect for Network
  - Review – AWS Blog and What’s New section of the website
  - Monitoring –  Amazon CloudWatch
Tradeoffs – Amazon Elasticache, Amazon CloudFront, AWS Snowball, Amazon RDS read replicas.

Key AWS service:
- Amazon CloudWatch

### Considerations

**PERF 1: How do you select the best performing architecture?**

Often, multiple approaches are required for optimal performance across a workload. Well-architected systems use multiple solutions and features to improve performance.

**PERF 2: How do you select your compute solution?**

The optimal compute solution for a workload varies based on application design, usage patterns, and configuration settings. Architectures can use different compute solutions for various components and enable different features to improve performance. Selecting the wrong compute solution for an architecture can lead to lower performance efficiency.

**PERF 3: How do you select your storage solution?**

The optimal storage solution for a system varies based on the kind of access method (block, file, or object), patterns of access (random or sequential), required throughput, frequency of access (online, offline, archival), frequency of update (WORM, dynamic), and availability and durability constraints.

Well-architected systems use multiple storage solutions and enable different features to improve performance and use resources efficiently.

**PERF 4: How do you select your database solution?**

The optimal database solution for a system varies based on requirements for availability, consistency, partition tolerance, latency, durability, scalability, and query capability. Many systems use different database solutions for various subsystems and enable different features to improve performance. 

Selecting the wrong database solution and features for a system can lead to lower performance efficiency.

**PERF 5: How do you configure your networking solution?**

The optimal network solution for a workload varies based on latency, throughput requirements, jitter, and bandwidth. Physical constraints, such as user or on-premises resources, determine location options. These constraints can be offset with edge locations or resource placement.

**PERF 6: How do you evolve your workload to take advantage of new releases?**

When architecting workloads, there are finite options that you can choose from. However, over time, new technologies and approaches become available that could improve the performance of your workload.

**PERF 7: How do you monitor your resources to ensure they are performing?**

System performance can degrade over time. Monitor system performance to identify degradation and remediate internal or external factors, such as the operating system or application load.

**PERF 8: How do you use tradeoffs to improve performance?**

When architecting solutions, determining tradeoffs enables you to select an optimal approach. Often you can improve performance by trading consistency, durability, and space for time and latency.


## [Security](https://wa.aws.amazon.com/wat.pillar.security.en.html)

The Security pillar includes the ability to protect data, systems, and assets to take advantage of cloud technologies to improve your security.

- The ability to protect information, systems, and assets while delivering business value through risk assessments and mitigation strategies.
- There are five best practice areas and tools for security in the cloud:
  - Identity and Access Management – IAM, Multi-Factor Authentication, AWS Organizations
  - Detective Controls – AWS CloudTrail, AWS Config, Amazon GuardDuty
  - Infrastructure Protection – Amazon VPC, Amazon CloudFront with AWS Shield, AWS WAF
  - Data Protection – ELB, Amazon Elastic Block Store (Amazon EBS), Amazon S3, and Amazon Relational Database Service (Amazon RDS) encryption, Amazon Macie, AWS Key Management Service (AWS KMS)
  - Incident Response – IAM, Amazon CloudWatch Events

Key AWS service:
- AWS Identity and Access Management (IAM)

### Considerations

**SEC 1: How do you securely operate your workload?**

To operate your workload securely, you must apply overarching best practices to every area of security. Take requirements and processes that you have defined in operational excellence at an organizational and workload level, and apply them to all areas. Staying up to date with recommendations from AWS, industry sources, and threat intelligence helps you evolve your threat model and control objectives. Automating security processes, testing, and validation allow you to scale your security operations.

**SEC 2: How do you manage identities for people and machines?**

There are two types of identities you need to manage when approaching operating secure AWS workloads. Understanding the type of identity you need to manage and grant access helps you ensure the right identities have access to the right resources under the right conditions.
- Human Identities: Your administrators, developers, operators, and end users require an identity to access your AWS environments and applications. These are members of your organization, or external users with whom you collaborate, and who interact with your AWS resources via a web browser, client application, or interactive command-line tools.
- Machine Identities: Your service applications, operational tools, and workloads require an identity to make requests to AWS services, for example, to read data. These identities include machines running in your AWS environment such as Amazon EC2 instances or AWS Lambda functions. You may also manage machine identities for external parties who need access. Additionally, you may also have machines outside of AWS that need access to your AWS environment.

**SEC 3: How do you manage permissions for people and machines?**

Manage permissions to control access to people and machine identities that require access to AWS and your workload. Permissions control who can access what, and under what conditions.

**SEC 4: How do you detect and investigate security events?**

Capture and analyze events from logs and metrics to gain visibility. Take action on security events and potential threats to help secure your workload.

**SEC 5: How do you protect your network resources?**

Any workload that has some form of network connectivity, whether it’s the internet or a private network, requires multiple layers of defense to help protect from external and internal network-based threats.

**SEC 6: How do you protect your compute resources?**

Compute resources in your workload require multiple layers of defense to help protect from external and internal threats. Compute resources include EC2 instances, containers, AWS Lambda functions, database services, IoT devices, and more.

**SEC 7: How do you classify your data?**

Classification provides a way to categorize data, based on criticality and sensitivity in order to help you determine appropriate protection and retention controls.

**SEC 8: How do you protect your data at rest?**

Protect your data at rest by implementing multiple controls, to reduce the risk of unauthorized access or mishandling.

**SEC 9: How do you protect your data in transit?**

Protect your data in transit by implementing multiple controls to reduce the risk of unauthorized access or loss.

**SEC 10: How do you anticipate, respond to, and recover from incidents?**

Preparation is critical to timely and effective investigation, response to, and recovery from security incidents to help minimize disruption to your organization.


---

**Resources**

- [Best practices, Well-architected audits, account setup](https://github.com/mguery/aws-well-architected)
- [AWS Well-Architected Framework – Five Pillars](https://tutorialsdojo.com/aws-well-architected-framework-five-pillars)
- [AWS Well-Architected Framework - PDF](https://docs.aws.amazon.com/wellarchitected/latest/framework/wellarchitected-framework.pdf)
- [Well-Architected Framework - List of Considerations (Google Docs)](https://docs.google.com/document/d/1af6aLecK1I3hpzxWBQ6sfo7xMeyCrp-rVDWpZ7tKo7A)
- [Well-Architected Framework - List of Considerations (GitHub Markdown)](https://github.com/mguery/aws-well-architected/blob/main/waf-considerations.md)
