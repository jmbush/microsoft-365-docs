---
title: Specify the cloud protection level for Microsoft Defender Antivirus
description: Set your level of cloud protection for Microsoft Defender Antivirus.
keywords: Microsoft Defender Antivirus, antimalware, security, defender, cloud, aggressiveness, protection level
search.product: eADQiWindows 10XVcnh
ms.pagetype: security
ms.prod: m365-security
ms.mktglfcycl: manage
ms.sitesec: library
localization_priority: normal
ms.topic: article
author: denisebmsft
ms.author: deniseb
ms.date: 08/26/2021
ms.reviewer: mkaminska
manager: dansimp
ms.custom: nextgen
ms.technology: mde
---

# Specify the cloud protection level

**Applies to:**

- [Microsoft Defender for Endpoint](/microsoft-365/security/defender-endpoint/)
- Microsoft Defender Antivirus

Cloud protection works together with Microsoft Defender Antivirus to deliver protection to your endpoints much faster than through traditional security intelligence updates. You can configure your level of cloud protection by using Microsoft Endpoint Manager (recommended) or Group Policy.

> [!NOTE]
> Selecting **High**, **High +**, or **Zero tolerance** could cause some legitimate files to be detected. If that happens, you can unblock the detected file or dispute that detection in the Microsoft 365 Defender portal.

## Use Microsoft Endpoint Manager to specify the level of cloud protection

1. Go to the Microsoft Endpoint Manager admin center ([https://endpoint.microsoft.com](https://endpoint.microsoft.com)) and sign in.

2. Choose **Endpoint security** > **Antivirus**.

3. Select an antivirus profile. (If you don't have one yet, or if you want to create a new profile, see [Configure device restriction settings in Microsoft Intune](/intune/device-restrictions-configure).

4. Select **Properties**. Then, next to **Configuration settings**, choose **Edit**.

5. Expand **Cloud protection**, and then in the **Cloud-delivered protection level** list, select one of the following:

    - **High**: Applies a strong level of detection.
    - **High plus**: Uses the **High** level and applies extra protection measures (might affect client performance).
    - **Zero tolerance**: Blocks all unknown executables.

6. Choose **Review + save**, and then choose **Save**. 

> [!TIP]
> Need some help? See the following resources:
> - [Configure Endpoint Protection](/mem/configmgr/protect/deploy-use/endpoint-protection-configure)
> - [Add endpoint protection settings in Intune](/mem/intune/protect/endpoint-protection-configure)
  

## Use Group Policy to specify the level of cloud protection

1.  On your Group Policy management machine, open the [Group Policy Management Console](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731212(v=ws.11)).

2. Right-click the Group Policy Object you want to configure, and then select **Edit**.

3.  In the **Group Policy Management Editor** go to **Computer Configuration** > **Administrative templates**.

4.  Expand the tree to **Windows Components** > **Microsoft Defender Antivirus** > **MpEngine**.

5.  Double-click the **Select cloud protection level** setting and set it to **Enabled**. Select the level of protection:

    - **Default blocking level** provides strong detection without increasing the risk of detecting legitimate files.
    - **Moderate blocking level** provides moderate only for high confidence detections
    - **High blocking level** applies a strong level of detection while optimizing client performance (but can also give you a greater chance of false positives).
    - **High + blocking level** applies extra protection measures (might affect client performance and increase your chance of false positives).
    - **Zero tolerance blocking level** blocks all unknown executables.

6. Select **OK**.

7. Deploy your updated Group Policy Object. See [Group Policy Management Console](/windows/win32/srvnodes/group-policy)

> [!TIP]
> Are you using Group Policy Objects on premises? See how they translate in the cloud. [Analyze your on-premises group policy objects using Group Policy analytics in Microsoft Endpoint Manager - Preview](/mem/intune/configuration/group-policy-analytics). 
  
## See also

[Why cloud protection should be enabled for Microsoft Defender Antivirus](why-cloud-protection-should-be-on-mdav.md)
