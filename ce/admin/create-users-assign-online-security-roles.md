---
title: "Create users in Dynamics 365 for Customer Engagement apps and assign security roles | MicrosoftDocs"
ms.custom: 
ms.date: 07/19/2019
ms.reviewer: 
ms.service: crm-online
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
applies_to: 
  - Dynamics 365 for Customer Engagement  (online)
  - Dynamics 365 for Customer Engagement  Version 9.x
ms.assetid: 5f21f288-f941-4ca0-a15f-a91cd9feee4d
caps.latest.revision: 4
author: jimholtz
ms.author: jimholtz
manager: kvivek
search.audienceType: 
  - admin
search.app: 
  - D365CE
  - Powerplatform
---
# Create users in Dynamics 365 for Customer Engagement apps and assign security roles

[!INCLUDE[cc-applies-to-update-9-0-0](../includes/cc_applies_to_update_9_0_0.md)]<br/>[!INCLUDE[cc_applies_to_on-prem-9_0_0](../includes/cc_applies_to_on-prem-9_0_0.md)]

You use the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)] to create user accounts for every user who needs access to Customer Engagement apps. The user account registers the user with [!INCLUDE[pn_ms_online_services_environment](../includes/pn-ms-online-services-environment.md)]. In addition to registration with the online service, the user account must be assigned a license in order for the user to have access to the service. Note that when you assign a user the global administrator or the service administrator role in the [!INCLUDE[pn_ms_online_services_environment](../includes/pn-ms-online-services-environment.md)], it automatically assigns the user the System Administrator security role in [!INCLUDE[pn_microsoftcrm](../includes/pn-dynamics-crm.md)] apps . [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Differences between the Microsoft Online services environment administrative roles and Dynamics 365 for Customer Engagement apps (online) security roles](../admin/grant-users-access.md#BKMK_O365CRMroles)  
  
<a name="BKMK_create_users"></a>   

## Create a user account  
 When you create a user account in the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], the system generates a user ID and temporary password for the user. You have the option to let the service send an email message to the user as clear text. Although the password is temporary, you may consider copying the information to send to the user through a more secure channel, such as from an email service that can digitally encrypt the contents. For step-by-step instructions for creating a [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] user account, see [Create or edit users in Office 365](http://go.microsoft.com/fwlink/p/?LinkId=255286).  
  
 ![Video symbol](../admin/media/video-thumbnail-4.png "Video symbol") Check out the following video: [Add People to Dynamics 365 for Customer Engagement](https://go.microsoft.com/fwlink/p/?linkid=836826).  
  
> [!NOTE]
>  When you create a user and assign a license in the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], the user is also created in Customer Engagement apps. The synchronization process between the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)] and Customer Engagement apps can take a few minutes to complete.  
> 
>  By entering a user ID and password, a user can access the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)] to view information about the service. However, the user will not have access to Customer Engagement apps until you assign at least one Customer Engagement apps security role to this user.  
> 
> [!TIP]
>  To force an immediate synchronization between the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)] and Customer Engagement apps, do the following:  
> 
> - Sign out of Customer Engagement apps and the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
> - Close all open browsers used for Customer Engagement apps and the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
> - Sign back in to Customer Engagement apps and the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
  
## User profile information

Some user profile information is maintained and managed in the [!INCLUDE [pn-office-365-admin-center](../includes/pn-office-365-admin-center.md)].  After you create or update a user, these user profile fields are automatically updated and synchronized in your Customer Engagement instances.

The following table shows the fields that are managed in the **Users** section of the [!INCLUDE [pn-office-365-admin-center](../includes/pn-office-365-admin-center.md)].

|Dynamics 365 for Customer Engagement apps user form  |Office 365 / Azure Active Directory user  |
|---------|---------|
|User Name     |Username         |
|Full Name     |First name + Last name         |
|Title     |Job title         |
|Primary Email*     |Email         |
|Main Phone     |Office phone         |
|Mobile Phone     |Mobile phone         |
|Fax     |Fax number         |
|Address     |Street address         |
|Address     |City         |
|Address     |State or province         |
|Address     |Country or region         |

*To prevent data loss, the Primary Email field does not automatically update and synchronize with Dynamics 365 for Customer Engagement apps (online).

The following are Office 365 user contact fields.

![Office 365 user contact info](media/office-365-contact-info.png "Office 365 user contact info")

<a name="BKMK_addlicense"></a>   

## Add a license to a user account  
 You can license the user when you create the user account, or you can license the user later. You must assign a license to every user account that you want to access the online service.  
  
 For step-by-step instructions, see [Assign, reassign, or remove licenses](http://go.microsoft.com/fwlink/p/?LinkId=255449).  
  
> [!IMPORTANT]
>  Licensed users must be assigned at least one [!INCLUDE[pn_microsoftcrm](../includes/pn-dynamics-crm.md)] apps security role to access Customer Engagement apps.  
  
 **About user licenses**  
  
- [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps uses user licenses to provide access to your organization. You need one user license per person with an active user record who logs into your organization.  
  
- When you add a new person, the **New user account** form displays the number of user licenses available. If you reach your limit, the **On** button is no longer available. You can add additional licenses by choosing **Billing** > **Purchase Services** from the left-side menu in the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
  
- An unaccepted invitation requires a user license until the invitation expires two weeks after it was issued.  
  
- If you have more user licenses than you are using, contact support to reduce the number of licenses. You cannot reduce the number of licenses to less than you are currently using or less than your offer allows. Any changes are reflected in your next billing cycle.  
  
- Each user license requires a unique Microsoft account, and every user who logs on to [!INCLUDE[pn_microsoftcrm](../includes/pn-dynamics-crm.md)] apps needs a license. Most [!INCLUDE [pn-crm-shortest](../includes/pn-crm-shortest.md)] apps subscriptions include a specific number of user licenses.  

> [!NOTE]
> There is a set of default security roles that are assigned to users based on the license and/or solution installed. These security roles only give users Read access to apps that are installed in the instance. For example, when a user is assigned the Dynamics 365 Customer Engagement Plan license and is synced to an instance that has the Customer Service Hub app, the user is automatically assigned the Customer Service app access security role. There is no data access permission granted to this role. The administrator is still required to assign the appropriate security role to the user in order for the user to view and interact with the data. 

<a name="BKMK_AssignSecurity"></a>   

## Assign a security role to a user  
 Security roles control a user’s access to data through a set of access levels and permissions. The combination of access levels and permissions that are included in a specific security role sets limits on the user’s view of data and on the user’s interactions with that data.  
  
 [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps provides a default set of security roles. If necessary for your organization, you can create new security roles by editing one of the default security roles and then saving it under a new name.  
  
 You can assign more than one security role to a user. The effect of multiple security roles is cumulative, which means that the user has the permissions associated with all security roles assigned to the user.  
  
 Security roles are associated with business units. If you have created business units, only those security roles associated with the business unit are available for the users in the business unit. You can use this feature to limit data access to only data owned by the business unit.  
  
 For more information about the difference between [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] administrator roles and Customer Engagement apps security roles, see [Grant users access to Microsoft Dynamics 365 for Customer Engagement apps (online) as a Microsoft Online service](../admin/grant-users-access.md).  
  
> [!IMPORTANT]
>  You must assign at least one security role to every Customer Engagement apps user. The service does not allow access to users who do not have at least one security role. Even if a user is a member of a team with its own security privileges, the user won’t be able to see some data and may experience other problems when trying to use the system.  

> [!NOTE]
> By default, a security role can only be assigned to users with an Enabled status. If you need to assign a security role to users who have a Disabled status, you can do so by enabling the allowRoleAssignmentOnDisabledUsers [OrgDBOrgSettings](https://support.microsoft.com/help/2691237/orgdborgsettings-tool-for-microsoft-dynamics-crm).

 In Customer Engagement apps:  
  
1.  Select **Settings** > **Security** > **Users**.  
  
2.  In the list, select the user or users that you want to assign a security role to.  
  
3.  Select **Manage Roles**.  
  
     Only the security roles available for that user's business unit are displayed.  
  
4.  In the **Manage User Roles** dialog box, select the security role or roles you want for the user or users, and then select **OK**.  
  
<a name="BKMK_assign_admin"></a>   

## (Optional) Assign an administrator role  
 You can share [!INCLUDE[pn_ms_online_services_environment](../includes/pn-ms-online-services-environment.md)] administration tasks among several people by assigning [!INCLUDE[pn_ms_online_services_environment](../includes/pn-ms-online-services-environment.md)] administrator roles to users you select to fill each role. You might decide to assign the global administrator role to a second person in your organization for times when you are not available.  
  
 There are five [!INCLUDE[pn_ms_online_services_environment](../includes/pn-ms-online-services-environment.md)] administrator roles with varying levels of permissions. For example, the password reset administrator role can reset user passwords only; the user management administrator role can reset user passwords as well as add, edit, or delete user accounts; and the global administrator role can add online service subscriptions for the organization and can manage all aspects of subscriptions. For detailed information about [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] administrator roles, see [Assigning Admin Roles](http://go.microsoft.com/fwlink/p/?LinkId=255444).  
  
> [!NOTE]
> [!INCLUDE[pn_ms_online_services_environment](../includes/pn-ms-online-services-environment.md)] administrator roles are valid only for managing aspects of the online service subscription. These roles don’t affect permissions within the Customer Engagement apps service.  
  
<a name="BKMK_enableuser"></a>   

## Enable or disable users  
 To enable a user, assign a license to the user and add a user to the security group that is associated with an instance of Customer Engagement apps. If you enable a user that was disabled, you must send a new invitation for the user to access the system.  
  
 To disable a user, remove a license from the user or remove the user from the security group that is associated with an instance of Customer Engagement apps. Removing a user from the security group doesn’t remove the user’s license. If you want to make the license available to another user, you have to remove the license from the disabled user.  
  
> [!NOTE]
> Removing all security roles from the user prevents the user from signing into and accessing Customer Engagement apps. However, it doesn’t remove the license from the user and the user remains in the list of the enabled users in Customer Engagement apps. Removing security roles from a user isn’t a recommended method of removing access to Customer Engagement apps.  
>
> When using a security group to manage enabling or disabling users or provisioning access to a Dynamics 365 org, nested security groups within a selected security group are not supported and ignored.
>
> You can [assign records](https://docs.microsoft.com/dynamics365/customer-engagement/basics/assign-record-user-team) to a disabled user and also [share reports](https://docs.microsoft.com/dynamics365/customer-engagement/basics/share-report-users-teams) and accounts with them. This can be useful when migrating on-premises versions to online. If you need to assign a security role to users who have a Disabled status, you can do so by enabling the allowRoleAssignmentOnDisabledUsers [OrgDBOrgSettings](https://support.microsoft.com/help/2691237/orgdborgsettings-tool-for-microsoft-dynamics-crm).

  
 You must be a member of an appropriate administrator role to do these tasks. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Assigning Admin Roles](http://go.microsoft.com/fwlink/p/?LinkId=255444)  
  
### Enable a user by assigning a license to the user and adding a user to the security group  
  
1. Browse to the [Microsoft 365 admin center](https://admin.microsoft.com) and sign in.  
  
2. Click **Users** > **Active users** and select the user.  
  
3. Under **Product licenses**, click **Edit**.  
  
4. Turn on a **[!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps** license, and then click **Save** > **Close**.  
  
5. In the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], click **Groups** > **Groups**.  
  
6. Choose the security group that is associated with your Customer Engagement apps organization.  
  
7. Under **Members**, click **Edit**, and then **Add members**. Select from the list of users with [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)] licenses or use **Search** to find users.  
  
8. Select the users to add to the security group, and then click **Save** > **Close** multiple times.  
  
    To add multiple users, see: [bulk add users to Office365 groups](http://go.microsoft.com/fwlink/p/?LinkID=615203).  
  
### Disable a user by removing a license from the user  
  
1. In the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], click **Users** > **Active Users** and select a user.  
  
2. In the right-side menu, under **Product licenses**, click **Edit**.  
  
3. Turn off the **[!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps ** license, and then click **Save** > **Close** multiple times.  
  
### Disable a user by removing the user from the security group that is associated with an instance of Dynamics 365 for Customer Engagement apps (online)  
  
1. In the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], click **Groups** > **Groups**.  
  
2. Choose the security group that is associated with your Customer Engagement apps organization.  
  
3. In the right-side menu, under **Members**, click **Edit**.  
  
4. Click **Remove members**, and then the select  users to remove from the security group.  
  
5. Click **Save** > **Close** multiple times.  
  
> [!NOTE]
> You can also delete users in the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)]. When you remove a user from your subscription, the license assigned to that user automatically becomes available to be assigned to a different user. If you want the user to still have access to other applications you manage through [!INCLUDE[pn_Office_365](../includes/pn-office-365.md)], for example [!INCLUDE[pn_Microsoft_Exchange_Online](../includes/pn-microsoft-exchange-online.md)] or [!INCLUDE[pn_ms_SharePoint_long](../includes/pn-ms-sharepoint-long.md)], don't delete them as a user. Instead, simply remove the [!INCLUDE[pn_microsoftcrm](../includes/pn-dynamics-crm.md)] apps license you've assigned to them.  
> 
> When you sign out of the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)], you aren’t signing out of [!INCLUDE [pn-crm-shortest](../includes/pn-crm-shortest.md)] apps. You have to do that separately.  

> [!TIP]
> To force an immediate synchronization between the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)] and Customer Engagement apps, do the following:  
> 
> - Sign out of Customer Engagement apps and the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
> - Close all open browsers used for Customer Engagement apps and the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
> - Sign back in to Customer Engagement apps and the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  

## Create a Read-Write user account
By default all licensed users are created with an access mode of **Read-Write**.  This access mode provides full access rights to the user based on the security privileges that are assigned. To update the access mode of a user:
1. Go to Customer Engagement apps.  
  
2. [!INCLUDE[proc_settings_security](../includes/proc-settings-security.md)]  
  
3. Choose **Users** > **Enabled Users**, and then click a user’s full name.  
  
4. In the user form, scroll down under **Administration**  to the **Client Access License (CAL) Information** section. In the **Access Mode** list, select **Read-Write**.  

5. Click the **Save** icon

## Create an Administrative user account
An Administrative user is a user who has access to the Settings and Administration features but has no access to any of the customer engagement functionality.  It is used to allow customers to assign administrative users to perform day-to-day maintenance functions (create user accounts, manage security roles, etc).  Since the administrative user does not have access to customer data and any of the customer engagement functionalities, it does not require a Dynamics 365 for Customer Engagement apps (online) license (after setup).

You need to have the System Administrator security role or equivalent permissions in Dynamics 365 for Customer Engagement apps to create an administrative user. First, you’ll create a user account in Office 365 and then in Dynamics 365 for Customer Engagement apps (online), select the **Administrative** access mode for the account.

> [!NOTE]
> See [Create an administrative user and prevent elevation of security role privilege](prevent-elevation-security-role-privilege.md) for an example of how an Administrative user account can be used.

1. [Create a user account](../admin/create-users-assign-online-security-roles.md#BKMK_create_users) in the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
  
    Be sure to assign a Customer Engagement apps license to the account. You'll remove the license (step 6) once you've assigned the **Administrative** access mode.
  
2. Go to Customer Engagement apps.  
  
3. [!INCLUDE[proc_settings_security](../includes/proc-settings-security.md)]  
  
4. Choose **Users** > **Enabled Users**, and then click a user’s full name.  
  
5. In the user form, scroll down under **Administration**  to the **Client Access License (CAL) Information** section. In the **Access Mode** list, select **Administrative**.  

    You then need to remove the Customer Engagement apps license from the account.  
  
6. Go to the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
  
7. Click **Users** > **Active Users**.  
  
8. Choose the Administrative user account and under **Product licenses**, click **Edit**.  
  
9. Turn off the Customer Engagement apps license,  and then click **Save** > **Close** multiple times.

<a name="BKMK_noninteractiveuser"></a>   

## Create a non-interactive user account  
 The non-interactive user is not a ‘user’ in the typical sense – it is not a person but an access mode that is created with a user account. It is used for programmatic access to and from Dynamics 365 for Customer Engagement apps between applications. A non-interactive user account lets these applications or tools, such as a Dynamics 365 for Customer Engagement apps to ERP connector, authenticate and access Dynamics 365 for Customer Engagement apps (online), without requiring a Dynamics 365 for Customer Engagement apps (online) license. For each instance of Dynamics 365 for Customer Engagement apps (online), you can create up to seven non-interactive user accounts.  
  
 You need to have the System Administrator security role or equivalent permissions in Dynamics 365 for Customer Engagement apps to create a non-interactive user. First, you’ll create a user account in Office 365 and then in [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)] apps, select the non-interactive access mode for the account.  
  
1. [Create a user account](../admin/create-users-assign-online-security-roles.md#BKMK_create_users) in the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
  
    Be sure to assign a Customer Engagement apps license to the account.  
  
2. Go to Customer Engagement apps.  
  
3. [!INCLUDE[proc_settings_security](../includes/proc-settings-security.md)]  
  
4. Choose **Users** > **Enabled Users**, and then click a user’s full name.  
  
5. In the user form, scroll down under **Administration**  to the **Client Access License (CAL) Information** section. In the **Access Mode** list, select **Non-interactive**.  
  
    You then need to remove the Customer Engagement apps license from the account.  
  
6. Go to the [!INCLUDE[pn_office_365_admin_center](../includes/pn-office-365-admin-center.md)].  
  
7. Click **Users** > **Active Users**.  
  
8. Choose the non-interactive user account and under **Product licenses**, click **Edit**.  
  
9. Turn off the Customer Engagement apps license,  and then click **Save** > **Close** multiple times.  
  
10. Go back to Customer Engagement apps and confirm that the non-interactive user account **Access Mode** is still set for **Non-interactive**.  
  
<a name="BKMK_ApplicationUser"></a>   

## Create an application user  
 Introduced in [!INCLUDE[pn_crm_8_2_0_online](../includes/pn-crm-8-2-0-online.md)], you can use server-to-server (S2S) authentication to securely and seamlessly communicate with [!INCLUDE[pn_crm_8_2_0_online_subsequent](../includes/pn-crm-8-2-0-online-subsequent.md)] with your web applications and services. S2S authentication is the common way that apps registered on [!INCLUDE[pn_microsoft_appsource](../includes/pn-microsoft-appsource.md)] use to access the [!INCLUDE[pn_crm_2016_shortest](../includes/pn-crm-2016-shortest.md)] data of their subscribers. All operations performed by your application or service using S2S will be performed as the application user you provide rather than as the user who is accessing your application.  

All application users are created with a non-interactive user account, however they are not counted towards the five non-interactive user accounts limit. In addition, there is no limit on how many application users you can create in an instance.
  
![Application user](../admin/media/application-user.png "Application user")  

## How stub users are created
A stub user is a user record that has been created as a placeholder. For example, records have been imported that refer to this user but the user does not exist in Dynamics 365 for Customer Engagement apps (online). This user cannot log in, cannot be enabled, and cannot be synchronized to Office 365. This type of user can only be created through data import. 

A default security role is automatically assigned to these imported users. The **Salesperson** security role is assigned in a Dynamics 365 for Customer Engagement instance and the **Common Data Service User** security role is assigned in a PowerApps environment.

> [!NOTE]
> By default, a security role can only be assigned to users with an Enabled status. If you need to assign a security role to users who have a Disabled status, you can do so by enabling the allowRoleAssignmentOnDisabledUsers [OrgDBOrgSettings](https://support.microsoft.com/help/2691237/orgdborgsettings-tool-for-microsoft-dynamics-crm). 


## Manage users in Microsoft Dynamics 365 (on-premises)

With Microsoft Dynamics 365 (on-premises), you can add users to your organization one at a time, or add multiple users at the same time by using the **Add Users** wizard.

### Add a user

1.  Go to **Settings** > **Security**.

2.  Choose **Users**.

3.  On the toolbar, choose **New**.

4.  On the **New User** page, in the **Account Information** section, specify the **User Name** for the user.

5.  In the **User Information** section, specify the **Full Name** for the user.

6.  In the **Organization Information** section, verify the **Business Unit** for the user.

7.  Follow the step for the task you’re doing:
    
      - To save the information for the new user, choose **Save**.
    
      - To save the information for the user and add another user, choose **Save & New**.
    
      - To add another user without saving the information you entered for the user, choose **New**, and then in the **Message from webpage** dialog box, choose **OK**.
    
    Next, you’ll need to assign a security role to the newly added user. See “Assign a security role to a user” later in this topic.

### Add multiple users

You can add multiple user records for the same set of security roles by using the Add Users wizard. Any users you add must be in the Active Directory directory service.

1.  Go to **Settings** > **Security**.

2.  Choose **Users**.

3.  On the toolbar, choose **New Multiple Users**.
    
    The **Add Users** wizard opens.

4.  On the **Select Security Roles** page, select one or more security roles, and then choose **Next**.

5.  On the **Select Access and License Type** page, under **Access Type**, select the appropriate access type for this set of users.

6.  Under **License Type**, specify the license type for this set of users.

7.  Under **Email Access Configuration**, specify how this set of users will access incoming and outgoing email messages, and then choose **Next**.

8.  On the **Select Domain or Group** page, specify to select users from all trusted domains and groups or users from a particular domain or group, and then choose **Next**.

9.  On the **Select Users** page, type a part of the name of user you want to add to Microsoft Dynamics 365. Use semi-colons between names.
    
10. Choose **Create New Users**.

11. On the **Summary** page, review the information about the user additions, and then follow the step for the task you are performing:
    
      - To close the Add Users wizard, choose **Close**.
    
      - If you need to add more users, for example with a different set of security roles, choose **Add More Users** to begin the wizard again.
    

    > [!NOTE]
    > To edit a specific user record, close the wizard, and then open the user record from the list.

### Assign a security role to a user

After you create users, you must assign security roles for them to use Microsoft Dynamics 365. Even if a user is a member of a team with its own security privileges, the user won’t be able to see some data and may experience other problems when trying to use the system. More information: [Security roles and privileges](security-roles-privileges.md)

1.  Go to **Settings** > **Security**.

2.  Choose **Users**.

3.  In the list, select the user or users that you want to assign a security role to.

4.  Choose **More Commands** (***...***) > **Manage Roles**.
    
    Only the security roles available for that user's business unit are displayed.

5.  In the **Manage User Roles** dialog box, select the security role or roles you want for the user or users, and then choose **OK**.


### Enable a user

1.  Go to **Settings** > **Security**.

2.  Select **Users**.

3.  Select the down arrow next to **Enabled Users**, and then choose **Disabled Users**.

4.  Select the checkmark next to the user you want to enable, and on the Actions toolbar, select **Enable**.

5.  In the **Confirm User Activation** message, select **Activate**.

## Disable a user

> [!NOTE]
> You can [assign records](https://docs.microsoft.com/dynamics365/customer-engagement/basics/assign-record-user-team) to a disabled user and also [share reports](https://docs.microsoft.com/dynamics365/customer-engagement/basics/share-report-users-teams) and accounts with them. This can be useful when migrating on-premises versions to online. If you need to assign a security role to users who have a Disabled status, you can do so by enabling the allowRoleAssignmentOnDisabledUsers [OrgDBOrgSettings](https://support.microsoft.com/help/2691237/orgdborgsettings-tool-for-microsoft-dynamics-crm).

1.  Go to **Settings** > **Security**.

2.  Choose **Users**.

3.  In the **Enabled Users** view, select the checkmark next to the user you want to disable.

4.  On the Actions toolbar, select **Disable**.

5.  In the **Confirm User Record Deactivation** message, select **Deactivate**.

### Update a user record to reflect changes in Active Directory

When you create a new user or update an existing user in Microsoft Dynamics 365 (on-premises), some fields in the Dynamics 365 user records, such as the name and phone number, are populated with the information obtained from Active Directory Domain Services (AD DS). After the user record is created in Dynamics 365, there is no further synchronization between Active Directory user accounts and Dynamics 365 user records. If you make changes to the Active Directory user account, you must manually edit the Dynamics 365 user record to reflect the changes.

1.  Go to **Settings** > **Security**.

2.  Choose **Users**.

3.  In the list, select the user you want to update, and then choose **Edit**.

The following table shows the fields that are populated on the Dynamics 365 user form (user record) from the Active Directory user account:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Dynamics 365 user form</p></th>
<th><p>Active Directory user</p></th>
<th><p>Active Directory object tab</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>User name</p></td>
<td><p>User logon name</p></td>
<td><p>Account</p></td>
</tr>
<tr class="even">
<td><p>First name</p></td>
<td><p>First name</p></td>
<td><p>General</p></td>
</tr>
<tr class="odd">
<td><p>Last name</p></td>
<td><p>Last name</p></td>
<td><p>General</p></td>
</tr>
<tr class="even">
<td><p>Main Phone</p></td>
<td><p>Telephone number</p></td>
<td><p>General</p></td>
</tr>
<tr class="odd">
<td><p>Primary Email</p></td>
<td><p>Email</p></td>
<td><p>General</p></td>
</tr>
<tr class="even">
<td><p>*Address</p></td>
<td><p>City</p></td>
<td><p>Address</p></td>
</tr>
<tr class="odd">
<td><p>*Address</p></td>
<td><p>State/province</p></td>
<td><p>Address</p></td>
</tr>
<tr class="even">
<td><p>Home phone</p></td>
<td><p>Home</p></td>
<td><p>Telephones</p></td>
</tr>
</tbody>
</table>

* The Dynamics 365 Address field is comprised of the values from the City and State/province fields in Active Directory.


### See also  
 [Manage subscriptions, licenses, and user accounts](../admin/manage-subscriptions-licenses-user-accounts.md)   
 [Assigning Admin Roles](http://go.microsoft.com/fwlink/p/?LinkId=255444)   
 [Add users to Office 365 for business](https://support.office.com/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc?ui=en-US&rs=en-US&ad=US)   
 [Security roles and privileges](../admin/security-roles-privileges.md)   
 [Manage Microsoft Dynamics 365 for Customer Engagement apps (online) licenses](../admin/manage-licenses.md)
