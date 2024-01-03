## New github Enterprise.
```
https://limeii.github.io/2022/11/deploy-on-multiple-environment-with-github-actions/
https://www.kevinboosten.dev/how-to-use-angular-environment-files-in-your-azure-devops-multi-stage-yml-release-pipeline
```
1. got to settings and enable allow all actions and reuseable workflows
2. set development as default repos
3. In the member provillages set to Write.
4. 



![image](https://github.com/jniranjanreddy/github-actions/assets/83489863/96946a01-3fec-42aa-afe6-9589840df3a0)

![image](https://github.com/jniranjanreddy/github-actions/assets/83489863/c5888df8-e553-4133-8564-d02985976a24)


## Static website
![image](https://github.com/jniranjanreddy/github-actions/assets/83489863/336c6461-bf95-4b12-b79a-4440743fa025)

## How to access azure within Github actions
```
1. create a service principal, which will generaete a json, then create a secret.
   az as sp create-for-rbac --name githubactions  --role contributor --scopes /subscriptions/bcc5f874-b014-494c-8d36-00c478cfc844 --sdk-auth

```

az webapp list --query "[?state=='running']"
