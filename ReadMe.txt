az webapp deployment user set --user-name jain-saurabh@hcl.com --password <password>
az group create --name myResourceGroup --location "northcentralus"
az appservice plan create --name myAppServicePlan --resource-group myResourceGroup --sku B1 --is-linux
az --% webapp create --resource-group myResourceGroup --plan myAppServicePlan --name <app_name> --runtime "DOTNETCORE|2.1" --deployment-local-git

While creating a web app using dotnet core 
1. dotnet new web
2. modify the .csproj file to targer core 2.1 instead of 2.2
3. dotnet restore
4. dotnet build/run

git remote add azure https://myappdemo20190214.scm.azurewebsites.net/myappdemo20190214.git
git push azure master


use git config credential.helper store to clear the credentials from previous repository
