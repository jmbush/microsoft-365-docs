---
title: Example of a phishing email attack
description: Step through an example analysis of an phishing attack.
keywords: incidents, alerts, investigate, correlation, attack, machines, devices, users, identities, identity, mailbox, email, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords: 
  - NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: 
  - M365-security-compliance
  - m365initiative-m365-defender
ms.topic: conceptual
search.appverid: 
  - MOE150
  - MET150
ms.technology: m365d
---
# Example of a phishing email attack

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

**Applies to:**
- Microsoft 365 Defender

Microsoft 365 Defender can help detect malicious attachments delivered via email. Since the [Office 365 Security and Compliance Center](https://protection.office.com/) integrates with Microsoft 365 Defender, security analysts can have visibility on threats coming in from Office 365, such as through email attachments.

For example, an analyst was assigned a multi-stage incident.
 
:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-incident.png" alt-text="Example of a multi-stage incident."::: 

In the **Alerts** tab of the incident, alerts from Defender for Office 365 and Microsoft Cloud App Security are displayed. The analyst can drill down into the Defender for Office 365 alerts by selecting the email messages alerts. The details of the alert are displayed on the side pane.

:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-alerts.png" alt-text="Example of an email alert.":::
 
By scrolling down further, more information is displayed, showing the malicious files and user that was impacted.

:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-impact.png" alt-text="Example of user and file impact of an email alert.":::
  
Selecting **Open alert page** takes you to the specific alert where various information can be viewed in greater detail by selecting the link. The actual email message can be viewed by selecting **View messages in Explorer** toward the bottom of the panel.
 
:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-event-explorer.png" alt-text="Example of the details of an alert."::: 

This takes the analyst to the Threat Management page where the email Subject, Recipient, Sender, and other information are displayed. **ZAP** under **Special Actions** tells the analyst that the Zero-hour auto purge feature was implemented. ZAP automatically detects and removes malicious and spam messages from mailboxes across the organization. For more information, see [Zero-hour auto purge (ZAP) in Exchange Online](../office-365-security/zero-hour-auto-purge.md).

Other actions can be taken on specific messages by selecting **Actions**. 
 
:::image type="content" source="../../media/first-incident-path-phishing/first-incident-phishing-actions.png" alt-text="Example of the other actions can be taken on email messages."::: 

## Next step

See the [identity-based attack](first-incident-path-identity.md) investigation path.

## See also

- [Incidents overview](incidents-overview.md)
- [Investigate incidents](investigate-incidents.md)
- [Manage incidents](manage-incidents.md)
