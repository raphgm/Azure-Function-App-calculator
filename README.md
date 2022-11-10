# Azure-Function-App-calculator
- Using Http Trigger to  call an Azure-Function-App that sums the value of x and y and inputs a result  

- The app is tested locally and later published to Azure and also tested in Azure using http as it's trigger.  
- The class  was renamed to sum  
- The function attribute was also renamed  to sum  
- The content of  run method was deleted  
- The logger was not deleted   
- Lines as shown below were added  
- int x =int.Parse(req.Query["x"]);  
- int y =int.Parse(req.Query["y"]);  

- int result = x + y;  

- return new OkobjectResult(result);  

- The parseInt method parses a value as a string and returns the first integer  

- more information about partInt can be gotten from this link      https://www.w3schools.com/jsref/jsref_parseint.asp  

- the sum was calculated in the local environment using the link that was thrown to the debugger
http://localhost:7071/api/sum?x=4&y=6  

- The sum was calculated in Azure platform using the link that was gotten from *get function url* in the function tab of azure function app that was created earlier     

- https://calculateor.azurewebsites.net/api/sum?code=EsRjPbim3qkRt8DrJdE9Wvc7lSrB4shbGedKoWazSVTpAzFuFfkX9A==&x=10&y=18

# Secondly-creating-Azure-Function App

- Azure Functions lets you run your code in a serverless environment without having to first create a virtual machine (VM) or publish a web application.   

- Sign in to the Azure portal with your Azure account.  
- In the search bar, enter Function App and Create.  
- On the Basics page, use the function app settings as specified in the following *Function App name- calculatortests and others at default with your proper Region selected.   
- On the Hosting page, enter the following settings. *Operating system- Windows *Plan- Consumption (Serverless-In this serverless hosting, you pay only for the time your functions run)   
- Select "Review + create" to review the app configuration selections.    
On the "Review + create" page, review your settings, and then select "Create" to provision and deploy the function app    
- Select "Go to resource" to view your new function app. You can also select Pin to dashboard. Pinning makes it easier to return to this function app resource from your dashboard.  
# Deploying from VS code to Azure  
- Search for "Publish" Select Azure / Right-click on the project in Solution Explorer and select "Publish" 
- Then select "Azure function App (windows)" Click Next. 
- Then choose Select Existing. 
- "Select Finish", and on the Publish page, select "Publish" to deploy the package containing your project files to your new function app in Azure.  
- After the deployment completes, the root URL of the function app in Azure is shown in the Publish tab.  
- From the left menu of the Function App window, select "Functions"
- Select "Get function url"  
- The sum was calculated in Azure platform using the link that was gotten from "Get function url" in the function tab of azure function app that was created earlier:     https://calculatortests.azurewebsites.net/api/Sum?  code=OSpJGrRT9wz8Pcgx3w8SdhM7mY6cGge_Vw1ZRW7tEIVCAzFu-EG8fg==&x=6&y=4  
- Thank you for Reading.  
