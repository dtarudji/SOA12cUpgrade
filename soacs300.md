<img class="float-right" src="images/j2c-logo.png">

# Lab 300 - SOA composite applications Deployment from Oracle JDeveloper

---

## Introduction

This is the third and final lab that is part of the **SOACS** workshop. 

In this lab, you will deploy the **`ValidatePayment`** composite from JDeveloper directly to SOACS and test it.

## Objectives

- Learn how to create deploy SOA composites from JDeveloper to SOACS

## Required Artifacts

- The following lab and the **ValidatePayment** composite configured in the previous lab.

## Pre-requisites

After provisioning the SOA Cloud Service instance, there are a few post-provisioning steps that
are required for deployment from JDeveloper to be successful.

**Create a host entry in your environment**

- Open a terminal by Right click and **Open in Terminal**.

    ![](images/jdevDeploy/image250.png)

- Enter ***su*** and enter Password as **oracle** when prompted.

- Open the hosts file. Enter the **etc** folder by typing **cd /root/** followed by **cd /etc**. Enter **vi hosts**.

    ![](images/jdevDeploy/image251.png)

- Add the **IP** and **Hostname** into the host file. Hit **Esc** on the keyboard and press **`i`** to edit. Add the entry, hit **Esc** followed by **`:wq`** and hit **Enter**.

    ![](images/jdevDeploy/image252.png)

- Verify the entry by typing **cat hosts**.

    ![](images/jdevDeploy/image253.png)

## High-Level Steps

-   Deploy the ValidatePayment Composite from JDeveloper

-	Test the project from EM console

## Steps in Detail

### Deploy the ValidatePayment Composite from JDeveloper

-   Right-click on the project name in the project menu - select **Deploy** and your **project name**. Make sure you have the project menu and not the application menu in order to see this option.

    ![](images/validatePayment/image100.png)

-	Select the first option **Deploy to Application Server**.

    ![](images/jdevDeploy/image229.png)

-	Click **Next**.

-	For our labs, we will deploy with Revision ID 1.0.
Select the checkboxes for **Mark composite revision as default** and **Overwrite any existing composites with the same revision ID**.

    ![](images/jdevDeploy/image230.png)

-   Click **Next**.

-   Click on the **`+`** icon to add our SOACS cloud instance.

    ![](images/jdevDeploy/image231.png)

-   Enter the connection name as **SOACS**.

    ![](images/jdevDeploy/image232.png)

-   Click **Next**.

-   Enter the server Username and Password.

    ![](images/jdevDeploy/image233.png)

-   Click **Next**.

-   Enter the **Hostname**, leave the ports as default, make sure the **Always use SSL** checkbox is selected. Enter the **WebLogic Domain** name.

    ![](images/jdevDeploy/image234.png)

-   Click **Next**.

-   Click on **Test Connection**.

    ![](images/jdevDeploy/image235.png)

-   Click **Accept This Session** when the certificate details popup.

    ![](images/jdevDeploy/image236.png)

-   Make sure all the 12 tests are successful.

    ![](images/jdevDeploy/image237.png)

-   Click **Next**.

-   View the summary of the connection and click **Finish**.

    ![](images/jdevDeploy/image238.png)

-   Select the newly created connection **SOACS**, make sure the **Overwrite modules of the same name** is checked.

    ![](images/jdevDeploy/image239.png)

-   Click **Next**.

-   Verify that the SOA servers are shown and selected.

    ![](images/jdevDeploy/image240.png)

-   Click **Next**.

-   Verify the deployment summary and click **Finish**.

    ![](images/jdevDeploy/image241.png)

-   Check the deployment logs and verify that the composite has been successfully deployed to SOACS.

    ![](images/jdevDeploy/image242.png)

### Test the project from EM console

**Refer to Lab 200 to test the deployed SOA composite from the Oracle EM FMWC.**

You have now successfully completed all the labs of the SOACS Developer Workshop.
