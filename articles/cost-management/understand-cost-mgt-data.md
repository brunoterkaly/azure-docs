---
title: Understand Azure Cost Management data | Microsoft Docs
description: This article helps you better understand what data is included in Azure Cost Management and how frequently it is processed, collected, shown, and closed.
services: cost-management
keywords:
author: bandersmsft
ms.author: banders
ms.date: 02/07/2019
ms.topic: conceptual
ms.service: cost-management
manager: micflan
ms.custom:
---

# Understand Cost Management data

This article helps you better understand what data is included in Azure Cost Management. And it explains how frequently data is processed, collected, shown, and closed. You're billed for Azure usage monthly. However, your Azure subscription type determines when your billing month ends. How often Cost Management receives usage data varies based on different factors. Such factors include how long it takes to process the data and how frequently Azure services emit usage to the billing system.

## Supported Microsoft offers

The following information shows the currently supported [Microsoft Azure offers](https://azure.microsoft.com/support/legal/offer-details/) in Azure Cost Management.  An Azure offer is the type of the Azure subscription that you have.

| Category  | **Offer name** | **Offer number** |
| --- | --- | --- |
| **Azure Germany** | [Azure Germany Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-de-0003p/) | MS-AZR-DE-0003P |
|**Azure Government**|Azure Government Enterprise|MS-AZR-USGOV-0017P|
| **Enterprise Agreement (EA)**| Enterprise Dev/Test | MS-AZR-0148P |
| **Enterprise Agreement (EA)** | [Microsoft Azure Enterprise](https://azure.microsoft.com/offers/enterprise-agreement-support-upgrade/) | MS-AZR-0017P |
| **Microsoft Developer Network (MSDN)** | [MSDN Platforms](https://azure.microsoft.com/offers/ms-azr-0062p/) | MS-AZR-0062P |
| **Pay-As-You-Go** | [Pay-As-You-Go](https://azure.microsoft.com/offers/ms-azr-0003p/) | MS-AZR-0003P |
| **Pay-As-You-Go** | [Pay-As-You-Go Dev/Test](https://azure.microsoft.com/offers/ms-azr-0023p/) | MS-AZR-0023P |
| **Pay-As-You-Go** | [Microsoft Partner Network](https://azure.microsoft.com/offers/ms-azr-0025p/) | MS-AZR-0025P |
| **Pay-As-You-Go** | [Microsoft Azure Sponsorship](https://azure.microsoft.com/offers/ms-azr-0036p/) | MS-AZR-0036P |
| **Pay-As-You-Go** | [Free Trial](https://azure.microsoft.com/offers/ms-azr-0044p/) | MS-AZR-0044P |
| **Pay-As-You-Go** | [Azure in Open](https://azure.microsoft.com/offers/ms-azr-0111p/) | MS-AZR-0111P |
| **Pay-As-You-Go** | [Azure for Students](https://azure.microsoft.com/offers/ms-azr-0170p/) | MS-AZR-0170P |
| **Pay-As-You-Go** | Azure Pass | MS-AZR-0120P, MS-AZR-0122P - MS-AZR-0125P, MS-AZR-0128P - MS-AZR-0130P |
| **Visual Studio** | [Visual Studio Enterprise – MPN](https://azure.microsoft.com/offers/ms-azr-0029p/) | MS-AZR-0029P |
| **Visual Studio** | [Visual Studio Professional](https://azure.microsoft.com/offers/ms-azr-0059p/) | MS-AZR-0059P |
| **Visual Studio** | [Visual Studio Test Professional](https://azure.microsoft.com/offers/ms-azr-0060p/) | MS-AZR-0060P |
| **Visual Studio** | [Visual Studio Enterprise](https://azure.microsoft.com/offers/ms-azr-0063p/) | MS-AZR-0063P |
| **Visual Studio** | [Visual Studio Enterprise: BizSpark](https://azure.microsoft.com/offers/ms-azr-0064p/) | MS-AZR-0064P |

The following table shows unsupported offers.

| Category  | **Offer name** | **Offer number** |
| --- | --- | --- |
| **Cloud Solution Provider (CSP)** | Microsoft Azure | MS-AZR-0145P |
| **Cloud Solution Provider (CSP)** | Azure Government CSP | MS-AZR-USGOV-0145P |
| **Cloud Solution Provider (CSP)** | Azure Germany in CSP for Microsoft Cloud Germany | MS-AZR-DE-0145P |
| **Pay-As-You-Go** | Azure for Students Starter | MS-AZR-0144P |
| **Support Plans** | Standard support | MS-AZR-0041P |
| **Support Plans** | Professional Direct support | MS-AZR-0042P |
| **Support Plans** | Developer support | MS-AZR-0043P |
| **Support Plans** | Germany support plan | MS-AZR-DE-0043P |
| **Support Plans** | Azure Government Standard Support | MS-AZR-USGOV-0041P |
| **Support Plans** | Azure Government Pro-Direct Support | MS-AZR-USGOV-0042P |
| **Support Plans** | Azure Government Developer Support | MS-AZR-USGOV-0043P |

If you don't see data for a subscription and you want to determine if your subscription falls under the supported offers, you can validate that your subscription is supported. To validate that an Azure subscription is supported, sign-in to the [Azure portal](https://portal.azure.com). Then select **All Services** in the left menu pane. In the list of services, select **Subscriptions**. In the subscription list menu, click on the subscription that you want to verify. Your subscription is shown on the Overview tab and you can see the **Offer** and **Offer ID**. The following image shows an example.

![Example of the Subscription Overview tab showing Offer and Offer ID](./media/understand-cost-mgt-data/offer-and-offer-id.png)

## Costs included in Cost Management

The following tables show data that's included or isn't in Cost Management.

**Account types**

| **Included** | **Not included** |
| --- | --- |
| Enterprise Agreement (EA) | Cloud Solution Provider (CSP) - For more information, see the [Partner Center overview](https://docs.microsoft.com/azure/cloud-solution-provider/overview/partner-center-overview). |
| Pay-as-you-go (PAYG) |   |
| Dev/test |   |
| Free and trial |   |
| Partner Network |   |
| Azure in Open | &nbsp;  |

**Cost and usage data**

| **Included** | **Not included** |
| --- | --- |
| Azure service usage<sup>1</sup> | Reservation purchases – For more information, see [APIs for Azure reservation automation](../billing/billing-reservation-apis.md). |
| Marketplace offering usage | Marketplace purchases – For more information, see [Third-party service charges](../billing/billing-understand-your-azure-marketplace-charges.md). |
|   | Support charges - For more information, see [Invoice terms explained](../billing/billing-understand-your-invoice.md). |
|   | Taxes - For more information, see [Invoice terms explained](../billing/billing-understand-your-invoice.md). |
|   | Credits - For more information, see [Invoice terms explained](../billing/billing-understand-your-invoice.md). |

<sup>1</sup> Azure service usage is based on reservation and negotiated prices.

**Metadata**

| **Included** | **Not included** |
| --- | --- |
| Resource tags<sup>2</sup> | Resource group tags |

<sup>2</sup> Resource tags are applied as usage is emitted from each service and aren't available retroactively to historical usage.

## Rated usage data refresh schedule

Cost and usage data is available in Cost Management + Billing in the Azure portal and [supporting APIs](https://aka.ms/costmgmt/docs). Keep the following points in mind as you review costs:

- Estimated charges for the current billing period are updated six times per day.
- Estimated charges for the current billing period can change as you incur more usage.
- Each update is cumulative and includes all the line items and information from the previous update.
- Azure finalizes or _closes_ the current billing period up to 72 hours (three calendar days) after the billing period ends.

The following examples illustrate how billing periods could end.

Enterprise Agreement (EA) subscriptions – If the billing month ends on March 31, estimated charges are updated up to 72 hours later. In this example, by midnight (UTC) April 4.

Pay-as-you-go subscriptions – If the billing month ends on May 15, then the estimated charges might get updated up to 72 hours later. In this example, by midnight (UTC) May 19.

### Rerated data

Whether you use the [Cost Management APIs](https://aka.ms/costmgmt/docs), PowerBI, or the Azure portal to retrieve data, expect the current billing period's charges to get re-rated, and consequently change, until the invoice is closed.

## Usage data update frequency varies

The availability of your incurred usage data in Cost Management depends on a couple of factors, including:

- How frequently Azure services (such as Storage, Compute, CDN, and SQL) emit usage.
- The time taken to process the usage data through the rating engine and cost management pipelines.

Some services emit usage more frequently than others. So, you might see data in Cost Management for some services sooner than other services that emit data less frequently. Typically, usage for services takes 8-24 hours to appear in Cost Management. Keep in mind that data for an open month gets refreshed as you incur more usage because updates are cumulative.

## See also

- If you haven't already completed the first quickstart for Cost Management, read it at [Start analyzing costs](quick-acm-cost-analysis.md).
