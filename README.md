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

## How to configure self hosted runner.
```
🧷 Step-by-Step Setup
✅ Step 1: Go to Your Repository
Navigate to the repository on GitHub.

Click on Settings > Actions > Runners.

Click "New self-hosted runner".

✅ Step 2: Choose OS and Architecture
Select:

OS: Windows / Linux / macOS

Architecture: x64, ARM64, etc.

GitHub will show you specific commands based on your OS.

✅ Step 3: Download and Configure the Runner
Example for Linux x64:

bash
Copy
Edit
# Create a directory
mkdir actions-runner && cd actions-runner

# Download the latest runner
curl -o actions-runner-linux-x64-2.317.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.317.0/actions-runner-linux-x64-2.317.0.tar.gz

# Extract the runner
tar xzf ./actions-runner-linux-x64-2.317.0.tar.gz

# Configure the runner (replace token and URL from GitHub setup instructions)
./config.sh --url https://github.com/your-org/your-repo --token YOUR_GENERATED_TOKEN
You will be prompted to:

Give the runner a name.

Choose a work folder.

Decide whether it should run as a service.

✅ Step 4: Start the Runner
bash
Copy
Edit
./run.sh
To run as a service (recommended for CI/CD), install it:

bash
Copy
Edit
sudo ./svc.sh install
sudo ./svc.sh start
On Windows, use config.cmd, run.cmd, and svc install accordingly.

🧪 Step 5: Test Your Runner
Add the following to your .github/workflows/ci.yml:

yaml
Copy
Edit
runs-on: self-hosted
You can also add labels during configuration and use them:

yaml
Copy
Edit
runs-on: [self-hosted, linux, my-label]
```
## How to run github actions locally, without github
```
see act_github_actions_locally file

```
