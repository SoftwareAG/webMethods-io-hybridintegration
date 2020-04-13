# webmethods-hybridintegration
# Description
This setup is going to explain step by step how to upload a webMethods Integration Server (IS) workflow to the Webmethods.io Integration (wm.io) cloud. After connecting both systems, on premise data can easily be uploaded to the cloud.

# Prerequisite
* webMethods Integration Server User & Example Workflow
* webMethods.io Integration User

# Setup
## webMethods Integration Server 
1.	Open webMethods Integration Server ‘Admin Console’.

    ![Admin Console](/images/admin-console-001.png "Admin Console")

2.	Go to the ‘webMethods Cloud’ tab. In case this is not available, get in touch with your SAG contact person regarding the Cloud package.

    ![webMethods Cloud](/images/admin-console-002.png "webMethods Cloud")

3.	Click ‘Settings’ and enter your webMethods.io Integration credentials to connect IS with wm.io.

  * Username
  * Password
  * webMethods.io Integration Cloud URL (Tenant name):
      * Germany: https://your-tenant-name.int-aws-de.webmethods.io/ 
      * US: https://your-tenant-name.int-aws-us.webmethods.io/

    ![webMethods Cloud Settings](/images/admin-console-003.png "webMethods Cloud Settings")

4.	Go to ‘Accounts’ and click ‘Create On-Premise Account’. Enter your Integration Server User information (e.g. Administrator). Add the following information:

  * Alias Name
  * Description
  * Run As User

    To validate the account, click ‘Test Account Settings’. In case you receive the following message ‘The account is valid’, please     click ‘Save Changes’.
  
    ![webMethods Cloud Accounts](/images/admin-console-003.png "webMethods Cloud Accounts")
  
5.	Go to ‘Applications’ and click ‘Define webMethods Cloud Application’. In this section the relevant flow can be chosen, which will be available in wm.io Integration.
Enter now following information:

  * Name (The name of the new cloud application)
  * Description

    Now you can see all available IS packages with the corresponding flows. Choose the flow you would like to upload. Every flow you select will be visible in wm.io Integration.

    Click ‘Save Changes’ to save the new ‘Cloud Application’.

    ![webMethods Cloud Applications](/images/admin-console-005.png "webMethods Cloud Applications")

6.	As a last step, please click the ‘Upload-Button’. The selected cloud application is now available at wm.io Integration.

    ![webMethods Cloud Applications](/images/admin-console-006.png "webMethods Cloud Applications")


## webMethods.io Integration
1.	Go to ‘webMethods.io Integration’ and login to your tenant, where you have uploaded your ‘Cloud Application’ previously. www.softwareag.cloud

2.	Start with an empty flow

    ![webMethodsio Flow](/images/webmethodsio-001.png "webMethodsio Flow")

3.	Search your ‘Cloud Application’ on the connector search box on the right side. Drag & drop the new connector to the empty workflow.

    ![webMethodsio Connector](/images/webmethodsio-002.png "webMethodsio Connector")

4.	Additionally please add the ‘Logger Connector’ and connect your cloud application to your logger. By adding the connector, the result will be logged.

    ![webMethodsio Connector](/images/webmethodsio-003.png "webMethodsio Connector")

5.	After connecting the applications to each other, click ‘Settings’ to configure the ‘Cloud Application’.

    ![webMethodsio Connector Settings](/images/webmethodsio-004.png "webMethodsio Connector Settings")

      Please select and enter:

    * Select Action (The flow you have selected on the Integration Server)
    * Name (Predefined from the Integration server but possible to rename)
    * Conect to Demo_App – (Select the ‘On-Prem User’ you chose previously)

    Click ‘Next’ to finish the application configuration.
  
    ![webMethodsio Connector Settings](/images/webmethodsio-005.png "webMethodsio Connector Settings")
  
6.	Click ‘Logger Settings’ to start the mapping.
  
    ![webMethodsio Connector Settings](/images/webmethodsio-006.png "webMethodsio Connector Settings")

    On the left side (incoming data) the ‘On-Prem Demo Application’ can be found and on the right side the ‘Logger’. Map via drag & drop the relevant data to the logger and log the data.

    ![webMethodsio Connector Mapping](/images/webmethodsio-007.png "webMethodsio Connector Mapping")

    Once mapping is done, please click the save button.
    
 7.	Now the workflow is ready for getting tested. Before starting the testing, save the workflow and rename it. 

    ![webMethodsio Connector Flow](/images/webmethodsio-008.png "webMethodsio Flow")
   
 8.	Click the ‘Arrow Button’ (next to the save button) to test the workflow. After running the workflow successfully, the result can be verified on the bottom.
 
    ![webMethodsio Flow Testing](/images/webmethodsio-009.png "webMethodsio Flow Testing")
 
 9.	Go to ‘Logger’ to see the result.
 
    ![webMethodsio Result](/images/webmethodsio-010.png "webMethodsio Result")
    
 ______________________
These tools are provided as-is and without warranty or support. They do not constitute part of the Software AG product suite. Users are free to use, fork and modify them, subject to the license agreement. While Software AG welcomes contributions, we cannot guarantee to include every contribution in the master project.

Contact us at [TECHcommunity](mailto:technologycommunity@softwareag.com?subject=Github/SoftwareAG) if you have any questions.

