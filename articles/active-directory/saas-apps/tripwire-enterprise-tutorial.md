---
title: Azure Active Directory SSO integration with Tripwire Enterprise
description: Learn how to configure single sign-on between Azure Active Directory and Tripwire Enterprise.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: CelesteDG
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: how-to
ms.date: 12/14/2022
ms.author: jeedes

---

# Azure Active Directory SSO integration with Tripwire Enterprise

In this article, you'll learn how to integrate Tripwire Enterprise with Azure Active Directory (Azure AD). Tripwire Enterprise is the leading compliance monitoring solution, using file integrity monitoring (FIM) and security configuration management (SCM). When you integrate Tripwire Enterprise with Azure AD, you can:

* Control in Azure AD who has access to Tripwire Enterprise.
* Enable your users to be automatically signed-in to Tripwire Enterprise with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

You'll configure and test Azure AD single sign-on for Tripwire Enterprise in a test environment. Tripwire Enterprise supports **IDP** initiated single sign-on.

## Prerequisites

To integrate Azure Active Directory with Tripwire Enterprise, you need:

* An Azure AD user account. If you don't already have one, you can [Create an account for free](https://azure.microsoft.com/free/?WT.mc_id=A261C142F).
* One of the following roles: Global Administrator, Cloud Application Administrator, Application Administrator, or owner of the service principal.
* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Tripwire Enterprise single sign-on (SSO) enabled subscription.

## Add application and assign a test user

Before you begin the process of configuring single sign-on, you need to add the Tripwire Enterprise application from the Azure AD gallery. You need a test user account to assign to the application and test the single sign-on configuration.

### Add Tripwire Enterprise from the Azure AD gallery

Add Tripwire Enterprise from the Azure AD application gallery to configure single sign-on with Tripwire Enterprise. For more information on how to add application from the gallery, see the [Quickstart: Add application from the gallery](../manage-apps/add-application-portal.md).

### Create and assign Azure AD test user

Follow the guidelines in the [create and assign a user account](../manage-apps/add-application-portal-assign-users.md) article to create a test user account in the Azure portal called B.Simon.

Alternatively, you can also use the [Enterprise App Configuration Wizard](https://portal.office.com/AdminPortal/home?Q=Docs#/azureadappintegration). In this wizard, you can add an application to your tenant, add users/groups to the app, and assign roles. The wizard also provides a link to the single sign-on configuration pane in the Azure portal. [Learn more about Microsoft 365 wizards.](/microsoft-365/admin/misc/azure-ad-setup-guides). 

## Configure Azure AD SSO

Complete the following steps to enable Azure AD single sign-on in the Azure portal.

1. In the Azure portal, on the **Tripwire Enterprise** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, select the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Screenshot shows how to edit Basic SAML Configuration.](common/edit-urls.png "Basic Configuration")

1. On the **Basic SAML Configuration** section, if you have **Service Provider metadata file** then perform the following steps:

	a. Click **Upload metadata file**.

    ![Screenshot shows how to upload metadata file.](common/upload-metadata.png "File")

	b. Click on **folder logo** to select the metadata file and click **Upload**.

	![Screenshot shows to choose metadata file.](common/browse-upload-metadata.png "Folder")

	c. After the metadata file is successfully uploaded, the **Identifier** and **Reply URL** values get auto populated in Basic SAML Configuration section.

1. Your Tripwire Enterprise application expects the SAML assertions in a specific format, which requires you to add custom attribute mappings to your SAML token attributes configuration. The following screenshot shows an example for this. The default value of **Unique User Identifier** is **user.userprincipalname** but Tripwire Enterprise expects this to be mapped with the user's email address. For that you can use **user.mailnickname** attribute from the list or use the appropriate attribute value based on your organization configuration.

	![Screenshot shows the image of token attributes.](common/default-attributes.png "Attributes")

1. On the **Set-up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

    ![Screenshot shows the Certificate download link.](common/metadataxml.png "Certificate")

1. On the **Set up Tripwire Enterprise** section, copy the appropriate URL(s) based on your requirement.

	![Screenshot shows to copy configuration appropriate URL.](common/copy-configuration-urls.png "Metadata")

## Configure Tripwire Enterprise SSO

To configure single sign-on on **Tripwire Enterprise** side, you need to send the downloaded **Federation Metadata XML** and appropriate copied URLs from Azure portal to [Tripwire Enterprise support team](mailto:support@tripwire.com). They set this setting to have the SAML SSO connection set properly on both sides.

### Create Tripwire Enterprise test user

In this section, you create a user called Britta Simon in Tripwire Enterprise. Work with [Tripwire Enterprise support team](mailto:support@tripwire.com) to add the users in the Tripwire Enterprise platform. Users must be created and activated before you use single sign-on.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options.

* Click on Test this application in Azure portal and you should be automatically signed in to the Tripwire Enterprise for which you set up the SSO.

* You can use Microsoft My Apps. When you click the Tripwire Enterprise tile in the My Apps, you should be automatically signed in to the Tripwire Enterprise for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Additional resources

* [What is single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)
* [Plan a single sign-on deployment](../manage-apps/plan-sso-deployment.md).

## Next steps

Once you configure Tripwire Enterprise you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Cloud App Security](/cloud-app-security/proxy-deployment-aad).