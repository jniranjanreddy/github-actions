## New github Enterprise.
```
https://limeii.github.io/2022/11/deploy-on-multiple-environment-with-github-actions/
https://www.kevinboosten.dev/how-to-use-angular-environment-files-in-your-azure-devops-multi-stage-yml-release-pipeline
```
1. got to settings and enable allow all actions and reuseable workflows
2. set development as default repos
3. In the member provillages set to Write.
4. 

![image](https://github.com/user-attachments/assets/f4eb7b54-fd16-4cbd-bcf5-c9933e8a6ea8)


![image](https://github.com/jniranjanreddy/github-actions/assets/83489863/96946a01-3fec-42aa-afe6-9589840df3a0)

![image](https://github.com/jniranjanreddy/github-actions/assets/83489863/c5888df8-e553-4133-8564-d02985976a24)


## Static website
![image](https://github.com/jniranjanreddy/github-actions/assets/83489863/336c6461-bf95-4b12-b79a-4440743fa025)

## How to access azure within Github actions..
```
1. create a service principal, which will generaete a json, then create a secret.
   PS C:\> az ad sp create-for-rbac --name githubactions  --role contributor --scopes /subscriptions/xxxxxxxxxxxxxxxxxxx --sdk-auth
   Option '--sdk-auth' has been deprecated and will be removed in a future release.
   Creating 'contributor' role assignment under scope '/subscriptions/bcc5f874-b014-494c-8d36-00c478cfc844'
   The output includes credentials that you must protect. Be sure that you do not include these credentials in your code or check the credentials into your source control. For more information, see https://aka.ms/azadsp-cli
   {
     "clientId": "xxxxxxxxxxxxxxxx",
     "clientSecret": "xxxxxxxxxxxxxx",
     "subscriptionId": "xxxxxxxxxxxxxxxxxxx",
     "tenantId": "xxxxxxxxxxxxxxxxxx",
     "activeDirectoryEndpointUrl": "https://login.microsoftonline.com",
     "resourceManagerEndpointUrl": "https://management.azure.com/",
     "activeDirectoryGraphResourceId": "https://graph.windows.net/",
     "sqlManagementEndpointUrl": "https://management.core.windows.net:8443/",
     "galleryEndpointUrl": "https://gallery.azure.com/",
     "managementEndpointUrl": "https://management.core.windows.net/"
   }

```

az webapp list --query "[?state=='running']"
