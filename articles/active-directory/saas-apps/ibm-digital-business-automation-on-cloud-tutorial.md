---
title: 'Tutorial: Azure Active Directory single sign-on (SSO) integration with IBM Digital Business Automation on Cloud | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and IBM Digital Business Automation on Cloud.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 11/21/2022
ms.author: jeedes
---

# Tutorial: Azure Active Directory single sign-on (SSO) integration with IBM Digital Business Automation on Cloud

In this tutorial, you'll learn how to integrate IBM Digital Business Automation on Cloud with Azure Active Directory (Azure AD). When you integrate IBM Digital Business Automation on Cloud with Azure AD, you can:

* Control in Azure AD who has access to IBM Digital Business Automation on Cloud.
* Enable your users to be automatically signed-in to IBM Digital Business Automation on Cloud with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* IBM Digital Business Automation on Cloud single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* IBM Digital Business Automation on Cloud supports **SP and IDP** initiated SSO.

## Add IBM Digital Business Automation on Cloud from the gallery

To configure the integration of IBM Digital Business Automation on Cloud into Azure AD, you need to add IBM Digital Business Automation on Cloud from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **IBM Digital Business Automation on Cloud** in the search box.
1. Select **IBM Digital Business Automation on Cloud** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

 Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, assign roles, as well as walk through the SSO configuration as well. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides)

## Configure and test Azure AD SSO for IBM Digital Business Automation on Cloud

Configure and test Azure AD SSO with IBM Digital Business Automation on Cloud using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in IBM Digital Business Automation on Cloud.

To configure and test Azure AD SSO with IBM Digital Business Automation on Cloud, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure IBM Digital Business Automation on Cloud SSO](#configure-ibm-digital-business-automation-on-cloud-sso)** - to configure the single sign-on settings on application side.
    1. **[Create IBM Digital Business Automation on Cloud test user](#create-ibm-digital-business-automation-on-cloud-test-user)** - to have a counterpart of B.Simon in IBM Digital Business Automation on Cloud that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **IBM Digital Business Automation on Cloud** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you have **Service Provider metadata file**, perform the following steps:
	
	a. Click **Upload metadata file**.

	b. Click on **folder logo** to select the metadata file and click **Upload**.

	c. Once the metadata file is successfully uploaded, the **Identifier** and **Reply URL** values get auto populated in IBM Digital Business Automation on Cloud section textbox:

	> [!Note]
	> If the **Identifier** and **Reply URL** values do not get auto populated, then fill in the values manually according to your requirement.

    > [!Note]
    > Customers can obtain the metadata file for their Cloud subscription from the [IBM Digital Business Automation on Cloud Client support team](mailto:supportbpmoncloud@us.ibm.com).

1. If you don't have **Service Provider metadata file**, on the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `https://www.automationcloud.ibm.com/isam/sps/<TENANT>/saml20`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://www.automationcloud.ibm.com/isam/sps/<TENANT>/saml20/login`

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://www.automationcloud.ibm.com/isam/sps/<TENANT>/login`

	> [!NOTE]
	> These values are not real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [IBM Digital Business Automation on Cloud Client support team](mailto:supportbpmoncloud@us.ibm.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/metadataxml.png)

1. On the **Set up IBM Digital Business Automation on Cloud** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to IBM Digital Business Automation on Cloud.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **IBM Digital Business Automation on Cloud**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you are expecting a role to be assigned to the users, you can select it from the **Select a role** dropdown. If no role has been set up for this app, you see "Default Access" role selected.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure IBM Digital Business Automation on Cloud SSO

To configure single sign-on on **IBM Digital Business Automation on Cloud** side, you need to send the downloaded **Federation Metadata XML** and appropriate copied URLs from Azure portal to [IBM Digital Business Automation on Cloud support team](mailto:supportbpmoncloud@us.ibm.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create IBM Digital Business Automation on Cloud test user

In this section, you create a user called Britta Simon in IBM Digital Business Automation on Cloud. Work with [IBM Digital Business Automation on Cloud support team](mailto:supportbpmoncloud@us.ibm.com) to add the users in the IBM Digital Business Automation on Cloud platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to IBM Digital Business Automation on Cloud Sign on URL where you can initiate the login flow.  

* Go to IBM Digital Business Automation on Cloud Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the IBM Digital Business Automation on Cloud for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the IBM Digital Business Automation on Cloud tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the IBM Digital Business Automation on Cloud for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](https://support.microsoft.com/account-billing/sign-in-and-start-apps-from-the-my-apps-portal-2f3b1bae-0e5a-4a86-a33e-876fbd2a4510).

## Next steps

Once you configure IBM Digital Business Automation on Cloud you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
