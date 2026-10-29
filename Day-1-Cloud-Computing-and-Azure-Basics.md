# Day 1: Cloud Computing and Azure Basics

## What is cloud computing?

Cloud computing is the delivery of computing services over the internet. Instead of buying and maintaining every server yourself, you can use services hosted in a cloud platform and pay according to the pricing model and usage.

Common cloud services include computing power, storage, databases, networking, and tools for building or running applications.

## Why use the cloud?

- **Scale when needed:** Add or reduce capacity as demand changes.
- **Pay for what you use:** Many services charge based on usage, though pricing varies by service.
- **Deploy quickly:** Create resources in minutes instead of purchasing and setting up physical hardware.
- **Reach users around the world:** Choose from cloud regions in different parts of the world.
- **Resilience options:** Use availability and backup features to help design reliable systems.

Cloud services do not automatically make an application secure, highly available, or inexpensive. Those outcomes depend on how the services are selected and configured.

## Cloud service models

| Model | What the provider manages | What you typically manage | Simple example |
|---|---|---|---|
| **IaaS** (Infrastructure as a Service) | Physical datacenter, hardware, and virtualization | Operating system, applications, and much of the configuration | A virtual machine |
| **PaaS** (Platform as a Service) | Infrastructure and much of the operating platform | Your application and its data | A managed app hosting service |
| **SaaS** (Software as a Service) | The application and underlying platform | How you use and configure the software | Web-based email |

The exact division of responsibility depends on the service. In general, the provider manages more as you move from IaaS toward SaaS.

## Cloud deployment types

- **Public cloud:** Services run on a cloud provider's infrastructure and are accessed over a network.
- **Private cloud:** Cloud-style infrastructure dedicated to one organization.
- **Hybrid cloud:** A combination of private or on-premises systems and public cloud services.

## What is Microsoft Azure?

Microsoft Azure is Microsoft's cloud platform. It offers services for computing, storage, databases, networking, identity, analytics, and more. You can manage Azure resources through the Azure portal, command-line tools, APIs, or infrastructure-as-code tools.

## A simple example

Imagine a meeting website. It might use a web app to serve pages, a database to store meeting details, and storage for uploaded files. In Azure, each of those parts could use a different Azure service. Those deployed services are called **resources**. Day 2 explains how Azure organizes them.

## Quick review

1. In your own words, what does cloud computing provide?
2. Which model gives you the most control over the operating system: IaaS, PaaS, or SaaS?
3. What does hybrid cloud combine?

## Short answers

1. Computing services such as servers, storage, and databases delivered over a network.
2. IaaS.
3. On-premises or private infrastructure with public cloud services.

## Sources

- [What is cloud computing? — Microsoft Azure](https://azure.microsoft.com/resources/cloud-computing-dictionary/what-is-cloud-computing/)
- [What are IaaS, PaaS, and SaaS? — Microsoft Azure](https://azure.microsoft.com/resources/cloud-computing-dictionary/what-is-iaas/)