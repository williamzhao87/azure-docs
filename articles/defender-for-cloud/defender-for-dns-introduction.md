---
title: Microsoft Defender for DNS - the benefits and features
description: Learn about the benefits and features of Microsoft Defender for DNS
ms.date: 01/10/2023
ms.topic: overview
ms.author: dacurwin
author: dcurwin
---

# Overview of Microsoft Defender for DNS

Microsoft Defender for DNS provides an additional layer of protection for resources that use Azure DNS's [Azure-provided name resolution](../virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances.md#azure-provided-name-resolution) capability. 

From within Azure DNS, Defender for DNS monitors the queries from these resources and detects suspicious activities without the need for any additional agents on your resources.

## Availability

|Aspect|Details|
|----|:----|
|Release state:|General availability (GA)|
|Pricing:|**Microsoft Defender for DNS** is billed as shown on the [pricing page](https://azure.microsoft.com/pricing/details/defender-for-cloud/)|
|Clouds:|:::image type="icon" source="./media/icons/yes-icon.png"::: Commercial clouds<br>:::image type="icon" source="./media/icons/yes-icon.png"::: Azure China 21Vianet<br>:::image type="icon" source="./media/icons/yes-icon.png"::: Azure Government|


## What are the benefits of Microsoft Defender for DNS?

Microsoft Defender for DNS detects suspicious and anomalous activities such as:

- **Data exfiltration** from your Azure resources using DNS tunneling
- **Malware** communicating with command and control servers
- **DNS attacks** - communication with malicious DNS resolvers 
- **Communication with domains used for malicious activities** such as phishing and crypto mining

A full list of the alerts provided by Microsoft Defender for DNS is on the [alerts reference page](alerts-reference.md#alerts-dns).

## Dependencies

Microsoft Defender for DNS doesn't use any agents. 


## Next steps

In this article, you learned about Microsoft Defender for DNS. 

To protect your DNS layer, enable Microsoft Defender for DNS for each of your subscriptions as described in [Enable enhanced protections](enable-enhanced-security.md).

> [!div class="nextstepaction"]
> [Enable enhanced protections](enable-enhanced-security.md)

For related material, see the following article: 

- Security alerts might be generated by Defender for Cloud or received from other security products. To export all of these alerts to Microsoft Sentinel, any third-party SIEM, or any other external tool, follow the instructions in [Exporting alerts to a SIEM](continuous-export.md).
