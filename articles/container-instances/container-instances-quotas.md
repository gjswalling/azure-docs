---
title: Azure Container Instances quotas and region availability
description: The default quotas and region availability of the Azure Container Instances service.
services: container-instances
author: dlepow

ms.service: container-instances
ms.topic: overview
ms.date: 12/17/2018
ms.author: danlep
---
# Quotas and region availability for Azure Container Instances

All Azure services include certain default limits and quotas for resources and features. The following sections detail the default resource limits for several Azure Container Instances (ACI) resources, as well as the availability of the ACI service in Azure regions.

## Service quotas and limits

[!INCLUDE [container-instances-limits](../../includes/container-instances-limits.md)]

## Region availability

Azure Container Instances is available in the following regions with the specified CPU and memory limits. Values are current at time of publication. For up-to-date information, use the [List Capabilities](/rest/api/container-instances/listcapabilities/listcapabilities) API. Availability and resource limits may differ when using Azure Container Instances with a [virtual network](container-instances-vnet.md) (preview) or with [GPU resources](container-instances-gpu.md) (preview).

| Location | OS | CPU | Memory (GB) |
| -------- | -- | :---: | :-----------: |
| Canada Central | Linux | 4 | 16 |
| East US, North Europe, West Europe, West US, West US 2 | Linux | 4 | 14 |
| Japan East | Linux | 2 | 8 |
| Australia East, East US 2, Southeast Asia | Linux | 2 | 7 |
| Central India, East Asia, North Central US, South Central US, South India | Linux | 2 | 3.5 |
| East US, West Europe, West US | Windows | 4 | 14 |
| Australia East, Canada Central, Central India, East Asia, East US 2, Japan East, North Central US, North Europe, South Central US, South India, Southeast Asia, West US 2 | Windows | 2 | 3.5 |

Container instances created within these resource limits are subject to availability within the deployment region. When a region is under heavy load, you may experience a failure when deploying instances. To mitigate such a deployment failure, try deploying instances with lower CPU and memory settings, or try your deployment at a later time.

Let the team know of additional regions required or increased CPU/Memory limits at [aka.ms/aci/feedback](https://aka.ms/aci/feedback).

For more information on troubleshooting container instance deployment, see [Troubleshoot deployment issues with Azure Container Instances](container-instances-troubleshooting.md).

## Next steps

Certain default limits and quotas can be increased. To request an increase of one or more resources that support such an increase, please submit an [Azure support request][azure-support] (select "Quota" for **Issue type**).

<!-- LINKS - External -->
[azure-support]: https://ms.portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/newsupportrequest
