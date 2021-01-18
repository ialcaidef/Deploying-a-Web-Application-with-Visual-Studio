## DEMO6_L1

### Deploying a Web Application with Visual Studio

#### Demonstration Steps

1. Click **Start**, type **Visual Studio**. From the search results, right-click **Visual Studio 2017**, and then select **Run as administrator**. In the **User Control** dialog box,  click **Yes**.

2. On the **File** menu, point to **New**, and then click **Project**.

3. In the **New Project** dialog box, on the navigation pane, expand the  **Installed** node, expand the **Visual C\#** node, click the **Web** node, and then in the list of templates, click **ASP.NET Core Web Application**.

4. In the **Name** box, type **MyWebSite**.

5. In the **Location** box, enter *[repository root]***\Allfiles\20487C\Mod06\DemoFiles\DeployWebApp**.

6. Clear the **Create directory for solution** check box, and then click **OK**.

7. In the **New ASP.NET Core Web Application - MyWebSite** dialog box, select **API**, and then click **OK**.

8. Open Microsoft Edge and go to **https://portal.azure.com**.

9. If a page appears asking for your email address, enter your email address, and then click **Next**. Wait for the **Sign In** page to appear, enter your email address and password, and then click **Sign In**.

   >**Note**: If during sign in, a page appears asking you to choose from a list of previously used accounts, select the account you previously used, and then enter your credentials.

10. In the left menu of the portal, click **App Services**.

11. In the action bar, click **Add**, select **Web App**, and then at the bottom of the third screen, click **Create**.

12. In the **App name** box, enter the name **mod6demo1***YourInitials* (Replace *YourInitials* with your initials). This is a unique value, which when combined with the **.azurewebsites.net** suffix is used as the URL to your web app.

13. In the **Resource Group** section, select **Create new**, and then change the name of the resource group to **BlueYonder.Demo.06**.

14. Click **App Service Plan/Location**, and then click **Create new**.

15. In the **App Service Plan** box, type **BlueYonderDemo06**.

16. In the **Location** list, select the region closest to your location.

17. In the **Pricing tier** section, select **D1 Shared**, and then click **OK**.

18. Click **Create**. The site is added to the **Web Apps** table and its status is set to **Creating**. 

19. After the status changes to **Running**, in **MyWebSite - Microsoft Visual Studio(Administrator)**, on the **View** menu, click **Server Explorer**.

20. In **Server Explorer**, right-click the **Azure** pane and select **Connect To Microsoft Azure Subscription**.

21. On the **Sign In** page, if a page appears asking you to choose from a list of previously used accounts, select the account you previously used, enter your credentials, and then click **Sign in**.

    >**Note**:	Wait until the sign-in process completes.
    >You only need to perform this step once to import your Microsoft Azure account settings to Visual Studio.
    >Now Visual Studio 2017 can display the list of Web Apps and Azure Cloud Services to which you can deploy the applications.

22. In **MyWebSite - Microsoft Visual Studio(Administrator)**, in **Solution Explorer**, right-click **MyWebSite** project, and then select **Publish**.

23. In the **Pick a publish target** dialog box, select **App Service**, then in the **Azure App Service** view, select the **Select Existing** option, and then click **Create Profile**.

24. In the **App Service** dialog box, expand the **BlueYonder.Demo.06** folder, select **mod6demo1[YourInitials]**, and then click **OK**.

25. Click **Publish**.

    >**Note**: Visual Studio publishes the application according to the settings that are provided in the profile file. After deployment completes, Visual Studio opens Internet Explorer and displays the web app. The deployment process is quick because the process only copies the content of the application to an existing virtual machine and does not need to wait for a new virtual machine to be created.

26. In the browser, navigate to the following URL:

    ```url
    http://mod6demo1{YourInitials}.azurewebsites.net/api/values
    ```

27. Verify that the response is in the format: **["***value1***","***value2***"]**.
