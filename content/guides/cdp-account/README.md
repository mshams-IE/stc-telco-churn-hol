# Cloudera on Cloud Tenant Access Guide

This section guides you through how to login to Cloudera managment console and how to set your workload credentials.

## Login to Hand-on-lab Environment : 

Login to the Hands-on-lab environment using the SSO URL and credentials assigned to you by your instructor.
   
   > **Note:** If at any point of time during the lab you are asked to login as your session timed out, please use the same SSO link again.

![CDP SSO Login](./CDP_login_SSO.png.png)

## Setting your CDP workload password :

Your workload, i.e. FreeIPA, credentials allows access to non-SSO interfaces and APIs within Cloudera on cloud.

Login to the Cloudera on cloud console. Click on your user name and then select `Profile`. Depending on the UI layout your user name is located either in the top right corner (newer UI layout) or bottom left corner (old UI).

![User Profile Button in newer UI](./select_user_profile.png)

On the user profile page, click `Set Workload Password`.

![Click to set workload password](./set_workload_password.png)

In the dialog box that appears, enter the new workload password twice and click `Set Workload Password`. A message appears saying that the password is set successfully.

Note this password as it will be required to specified in later exercises.

!!! note
    Further details on how to set your workload password are available in the [Setting the workload password](https://docs.cloudera.com/management-console/cloud/user-management/topics/mc-setting-the-ipa-password.html){target="_blank"} documentation page.
