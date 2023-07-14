# JoeCalculatorFunctionApp  
- sign up or log in to your existing Azure account
- On the search bar type function app and select from the dropdown, then create.
- On the basic page, select a subscription, resource group, or create one.
- In the instance detail, Name the Function app, we are using JosCalculatorFunctionApp
- Leave other settings as default
- For Operating System select  window.
- For Hosting select consumption model.
- Then "Review + Create" button. Then "Create" to provision and deploy the function app.
- Select "Go to resources" to view the newly created function app.

### Steps To Create A Function App Using Visual Studio  
- Launch visual studio from your local machine, at the right pane, select "Create
- new project".
- In the search bar "type azure function" and select.
- In the next window provide your application a name and Click the Create button
- A new window appears, select "HTTPS Trigger"- this is selected because we want our app to be seen on the browser).
- Click the Create button and wait for our application to be created.

 
 We have created our Function app. To code a simple sum application that can add two numbers x and y, we follow his guide.
- The class is renamed to "JoeCalcFunctApp".
- The function attribute was also renamed to "JoeCalcFunctApp".
- Delete the content of the run method.
- Add the lines of code shown below.
  ```
    int x = int.Parse(req.Query["x"]);
    int y = int.Parse(req.Query["y"]);
    int result = x + y;

    return new OkobjectResult(result);
  ```

The ParseInt method parses a value as a string and returns an Integer.  
- Right-click on "JoeCalcFunctApp" on the right pane, and select Build.
- The Function App was built successfully.

### Publishing The Function APP to Azure
- Right-click on "JoeCalcFunctApp" on the right pane and select Publish.
- In the publish target select Azure, and click next.
- In select "Publish specific target", select Azure function and click next.
- In the function Instance window, select your existing subscription.
- Click the publish button.

### Testing your Function App on A Browser.  
- Open the Azure portal and select Function app from the home screen.
- Click on the App to open it and copy the URL.
- paste the copied URL on a browser, and give "x" and "y" a value.
- Example on your browser screen `https://joscalculatorfunctionapp.azurewebsites.net/api/JoeCalcFunctApp?code=VwTTBZ0K9RQv_Lpa5-wl5Qs1X1nbeXaNrTZchmYU-T2FAzFu7qrymA==&x=400%20&y=200`

### Pushing Files To GitHub  
- Log in to your GitHub account, on the dashboard click the "New" button.
- In the create repository, give the file a name. Make sure the Readme button is ticked, and the repository is Public.
- Open your Azure portal , then the function App, scroll down to deployment and click open.
- Select deployment center, for "Source",select the drop-down arrow and select Github and select"Authorize" button below.
- Click the authorize azure application button and enter your password.
- On your Azure Function App, select and click deploy. Wait for the process
Congratulation you hav succeded in deploying your first Function applicaton to Azure.

