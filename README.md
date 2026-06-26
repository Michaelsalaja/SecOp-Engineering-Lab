# Connecting Logs to Microsoft Sentinel using Data Connectors

## Introduction

This SecOp Engineering lab demonstrates how to connect logs to an enterprise Microsoft Sentinel as a Security Engineer or as an Analyst in a Security Operations Center for any organization that has implemented Microsoft Sentinel beforehand. It creates clear picture that mirrors the trajectory to understanding the connection of log data from many data sources in your organization. We could imagine your organization having data from Microsoft 365, Microsoft Defender XDR, Azure resources, non-azure virtual machines, etc. We also must ensure that the log connection operation meets the company requirements to minimize cost, meet compliance regulations, and provide the most manageable environment for your security team to perform their daily job responsibilities.

## Connect Data to Microsoft Sentinel using Data Connectors

After obtaining my Microsoft 365 Credentials as the first step, I opened Microsoft Edge browser to login into the Microsoft Defender XDR portal. In this task, my goal is to manage the Microsoft Defender for Cloud data connector.

## Objective 1

### Step 1

* In the Microsoft Defender navigation menu, I scrolled down and expanded the Microsoft Sentinel section.

* I expanded the **Content management** section and selected **Content Hub**.

* Various data connectors can be seen in the picture below under **Content Title**, including their status, content source, provider, support, and category.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%201.png)

Figure 1: Screenshot of Microsoft Defender portal showing the Home dashboard with Microsoft Sentinel integration


## Step 2

* In the **Content hub**, I searched for the Microsoft Defender for Cloud solution.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%202.png)

Figure 2: Screenshot of Microsoft Defender Content hub interface showing a list of installed solutions like Amazon Web Services, Azure Activity, and Microsoft Defender for Cloud.



**Step 3**

* I selected it from the list, given the fact that this task is focused on Cloud data connector.

* On the Microsoft Defender for Cloud solution details page, selected **Manage**.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%203.png)

Figure 3: Screenshot of Microsoft Defender Content hub interface


This enabled the installation of Microsoft Defender for Cloud solution:

* Subscription-based Microsoft Defender for Cloud (Legacy) Data connector,

* Tenant-based Microsoft Defender for Cloud (Preview) Data connector

* An Analytics rule.

It is important to note that the Tenant-based Microsoft Defender for Cloud (Preview) Data connector is used when a tenant has multiple subscriptions, so I selected the **Tenant-based Microsoft Defender for Cloud Data connector check-box** and clicked on **Open connector page** once.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%204.png)

Figure 4: Screenshot of Microsoft Defender for Cloud Content hub in Microsoft Sentinel

* A new browser tab opens up on the Azure portal Data Connector page and the status shows show Connected, which validates the integration of Tenant-based Microsoft Defender for Cloud data connector.

* It is essential that the **Configuration** section of the Instructions tab is reviewed to be aware of the requirements and instructions. One thing that must be pinpointed is that "Microsoft Defender for Cloud alerts are connected to stream through the Microsoft 365 Defender" now, and that you "Cannot disconnect while Microsoft Defender XDR is connected".

* The **Details pane** also shows that **Data types** use SecurityAlert table, which will be explored in my upcoming projects.
  
![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%205.png)

Figure 5: Screenshot of the Microsoft Azure portal showing the Tenant-based Microsoft Defender for Cloud connector configuration page

* I closed the browser tab and returned to Microsoft Defender XDR to connect Azure Activity solution as the next connector.

**Task 2**

Step 1

* Continuing from the Microsoft Sentinel **Content Hub** home page, where I was before, I searched for the Azure Activity solution and selected it from the list.

* On the Azure Activity solution details page on the right-hand side, I selected **Manage**. Clicking **Manage** will trigger the Azure Activity solution to install the **Azure Activity Data connector**, **13 Analytic rules**, **14 Hunting queries** and **1 Workbook**

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%206.png)

Figure 6: Screenshot of Microsoft Defender Content hub showing Azure Activity solution details

**Step 2**

I selected the **Azure Activity** Data connector and select **Open connector page**.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%207.png)

Figure 7: Screenshot of Microsoft Defender Sentinel Content Hub

* The status shows that Azure Activity connector is intact.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%208.png)

Figure 8: Screenshot Microsoft Defender Sentinel Connector Details


* This data connector is fully ported to Defender XDR.

* When the box is checked in the Setup tab under Table management section, the *Gear wheel* for Data Retention settings emerges, which we could not see in the above picture, but in the one below

* I clicked the Data Retention Settings to review and manage AzureActivity settings in Analytics tier.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%209.png)

Figure 9: Screenshot of Microsoft Defender portal showing Azure Activity connector details and table management settings.


* In the *Manage AzureActivity* in Analytics tier in the screenshot below, the data retention can be changed at any given time

* I closed out of the *Manage AzureActivity* page by selecting the **X** in the upper right corner.

* This data connector is fully ported to Defender XDR.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%2010.png)

Figure 10: Screenshot of Microsoft Defender for Cloud portal showing Azure Activity data connector page with a side panel for Manage AzureActivity settings.

* To review and configure the Configure UEBA settings. Note that this setting is enabled for \*Azure Activity, I selected Advanced Features next to the Setup tab.

* The notification pops up showing that Azure the setting is enabled for \*Azure Activity.

![image alt](https://github.com/Michaelsalaja/SecOp-Engineering-Lab/blob/90bc6f9f3954f795eef8a16b3cc968f792152193/Figure%2011.png)

Figure 11: Screenshot of Microsoft Defender portal showing Azure Activity data connector details and UEBA configuration

## Summary

This shot labs helped sharpen my practical understanding of how to ingest data to Microsoft Sentinel using Data Connectors. I executed the following tasks for this Security Operations.

* Green sphere icon Accessed the Microsoft Sentinel Workspace on the Microsoft Defender portal

* Green sphere icon Connected log data from different log sources

* Green sphere icon Used the Content Hub solution to provision Microsoft Sentinel Data connectors

* Green sphere icon Managed the Microsoft Defender for Cloud data connector by installing a Tenant-based Microsoft Defender for Cloud (Preview) Data connector

* Green sphere icon Connected Azure Activity data connector to Microsoft Sentinel

* Green sphere icon Managed the Azure Activity data connector containing 13 Analytic rules, 14 Hunting queries and 1 Workbook

* Green sphere icon Reviewed and configured User Entity Behavioral Analytics (UEBA) for the Azure Activity

* Green sphere icon Enabled the Defender XDR connector in Microsoft Sentinel.

* Green sphere icon I skipped the exploration of Azure Active Directory and Azure Active Directory Identity Protection because the steps for connecting Audi and Sign-in logs to Microsoft Sentinel is quite identical to the connection of Azure Activity to Microsoft Sentinel.

## Follow-up

Now that my mission to connect and ingest data to Microsoft Sentinel using Data connectors as objective one has been accomplished, I advanced to objective 2.

In my next project, I will be connecting data from Windows virtual machines inside and outside of Azure, like on-premises environments or other Public Clouds as the next source of data.
