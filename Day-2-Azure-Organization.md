# Day 2: Azure Organization

Azure uses a hierarchy to organize resources and manage access, policy, and costs. A useful simplified view is:

```text
Microsoft Entra tenant
└── Management group(s)
    └── Subscription(s)
        └── Resource group(s)
            └── Resource(s)
```

A tenant is the identity boundary for users and applications. This lesson focuses on the four Azure organization levels below it.

## 1. Management groups

A **management group** organizes multiple Azure subscriptions. Organizations can assign governance rules, such as Azure Policy or access controls, at a management group scope so they can apply to subscriptions beneath it.

**Think of it as:** An organization-wide folder for subscriptions, with shared rules.

**Example:** A company could place its production subscriptions under a Production management group and apply approved-location rules there.

The user's Day 2 practice answer was **Management Group**. That is the right concept when the question is asking for the layer used to organize subscriptions and apply governance across them.

## 2. Subscriptions

An Azure **subscription** is a boundary for organizing resources, access, and billing. Resources are deployed into a subscription. A subscription can contain many resource groups.

**Think of it as:** A managed account or boundary that helps separate workloads and track costs.

**Example:** A company might have separate subscriptions for development and production.

A subscription is not the same thing as an Azure account login. A person may have access to one or more subscriptions.

## 3. Resource groups

A **resource group** is a logical management container for Azure resources. It helps you manage related resources together, for example by assigning access, applying tags, deploying resources, and deleting a set of resources when appropriate.

**Think of it as:** A project box for related Azure resources.

**Meeting website example:** The website's app service, database, and storage account could be placed in a resource group called `meeting-site-prod` if they share a management lifecycle.

A resource group is not a physical network container. Resources in it can have their own deployment regions, and resources can sometimes depend on or connect to resources in other groups. Choose group boundaries based on management and lifecycle needs.

## 4. Resources

A **resource** is an individual Azure service or component that you create and manage.

Examples include:

- A virtual machine
- A storage account
- A virtual network
- A database
- A web app

**Think of it as:** One building block used by your solution.

## 5. Regions

An Azure **region** is a geographic area containing one or more Azure datacenters. When a service supports your chosen region, you select a location for that resource.

Companies often consider a region near their users to reduce network latency, which can make responses feel faster. Region choice should also consider service availability, data residency and compliance requirements, reliability design, and cost. The closest region is not automatically the best choice for every workload.

A resource group's location is metadata for the group itself; it does not automatically force every resource in that group to be deployed in that same region.

## Put it together

For the meeting website, a simple example might be:

- **Management group:** `Online-Workloads`
- **Subscription:** `MeetingSite-Production`
- **Resource group:** `meeting-site-prod`
- **Resources:** Web app, database, and storage account
- **Regions:** Selected for each resource based on users, requirements, and service availability

This is only an example. Real designs can use more subscriptions and resource groups as the organization grows.

## Quick review

1. Which level groups subscriptions and can carry governance rules for them?
2. Which level is used for billing and resource organization boundaries?
3. What is a resource group used for?
4. Name two examples of Azure resources.
5. Why might an organization choose a region near its customers?

## Short answers

1. Management group.
2. Subscription.
3. To logically group related resources for management, access, tagging, and lifecycle tasks.
4. For example, a virtual machine and a storage account.
5. To reduce network latency, while also considering compliance, availability, and cost.

## Sources

- [Organize your resources with management groups — Microsoft Learn](https://learn.microsoft.com/azure/governance/management-groups/overview)
- [Azure resource management fundamentals — Microsoft Learn](https://learn.microsoft.com/entra/architecture/secure-resource-management)
- [Azure resource organization — Microsoft Cloud Adoption Framework](https://learn.microsoft.com/azure/cloud-adoption-framework/ready/azure-setup-guide/organize-resources)
- [Azure regions — Microsoft Cloud Adoption Framework](https://learn.microsoft.com/azure/cloud-adoption-framework/ready/considerations/regions)
