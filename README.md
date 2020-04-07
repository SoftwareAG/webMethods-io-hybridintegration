# webmethods-hybridintegration
# Description
This setup is going to explain step by step how to upload a webMethods Integration Server (IS) workflow to the Webmethods.io Integration (wm.io) cloud. After connecting both systems, on premise data can easily be uploaded to the cloud.
# Setup
## webMethods Integration Server 
1.	Open webMethods Integration Server ‘Admin Console’.
[BILD]
2.	Go to the ‘webMethods Cloud’ tab. In case this is not available, get in touch with your SAG contact person regarding the Cloud package.
[BILD]
3.	Click ‘Settings’ and enter your webMethods.io Integration credentials to connect IS with wm.io.
* Username
* Password
* webMethods.io Integration Cloud URL (Tenant name)
Germany: https://your-tenant-name.int-aws-de.webmethods.io/ 
US: https://your-tenant-name.int-aws-us.webmethods.io/
[BILD]

4.	Go to ‘Accounts’ and click ‘Create On-Premise Account’. Enter your Integration Server User information (e.g. Administrator). Add the following information:
* Alias Name
* Description
* Run As User

  To validate the account, click ‘Test Account Settings’. In case you receive the following message ‘The account is valid’, please     click ‘Save Changes’.
  [BILD]
  
5.	Go to ‘Applications’ and click ‘Define webMethods Cloud Application’. In this section the relevant flow can be chosen, which will be available in wm.io Integration.
Enter now following information:

* Name (The name of the new cloud application)
* Description

  Now you can see all available IS packages with the corresponding flows. Choose the flow you would like to upload. Every flow you select will be visible in wm.io Integration.
Click ‘Save Changes’ to save the new ‘Cloud Application’.
[BILD]

6.	As a last step, please click the ‘Upload-Button’. The selected cloud application is now available at wm.io Integration.
[BILD]

## webMethods.io Integration
1.	Go to ‘webMethods.io Integration’ and login to your tenant, where you have uploaded your ‘Cloud Application’ previously. www.softwareag.cloud

2.	Start with an empty flow
[BILD]

3.	Search your ‘Cloud Application’ on the connector search box on the right side. Drag & drop the new connector to the empty workflow.
[BILD]

4.	Additionally please add the ‘Logger Connector’ and connect your cloud application to your logger. By adding the connector, the result will be logged.
[BILD]

5.	After connecting the applications to each other, click ‘Settings’ to configure the ‘Cloud Application’.
[BILD]
Please select and enter:

* Select Action (The flow you have selected on the Integration Server)
* Name (Predefined from the Integration server but possible to rename)
* Conect to Demo_App – (Select the ‘On-Prem User’ you chose previously)

  Click ‘Next’ to finish the application configuration.
  [BILD]
  
6.	Click ‘Logger Settings’ to start the mapping.
  [BILD]
    On the left side (incoming data) the ‘On-Prem Demo Application’ can be found and on the right side the ‘Logger’. Map via drag & drop the relevant data to the logger and log the data.
    [BILD]
    Once mapping is done, please click the save button.
    
 7.	Now the workflow is ready for getting tested. Before starting the testing, save the workflow and rename it. 
   [BILD]
   
 8.	Click the ‘Arrow Button’ (next to the save button) to test the workflow. After running the workflow successfully, the result can be verified on the bottom.
 [BILD]
 
 9.	Go to ‘Logger’ to see the result.
 [BILD]
    
  

