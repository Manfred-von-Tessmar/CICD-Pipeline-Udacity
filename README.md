# Overview

In this project a CICD-Pipeline was set up with Azure Pipelines. 

## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project
* A link to a spreadsheet that includes the original and final project plan>

## Instructions

<TODO:  
* Architectural Diagram (Shows how key parts of the system work)>

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

![azure_app_service](https://user-images.githubusercontent.com/92888738/148787976-75ef3494-bafe-4309-8fd6-18a5d4eabb8f.PNG)

* Project cloned into Azure Cloud Shell

![github_repo_in_azurecloudshell](https://user-images.githubusercontent.com/92888738/148787588-0244ee46-a4ba-4b33-8e13-23d14a5a5276.PNG)

* Passing tests that are displayed after running the `make all` command from the `Makefile`

![maketest](https://user-images.githubusercontent.com/92888738/148789121-e45e2bad-b0a8-4623-81a2-44ad33578b5f.PNG)

* Output of a test run

 

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

![implement_pipelines_to_azure](https://user-images.githubusercontent.com/92888738/149521983-0c01a940-7820-48e5-814d-cd832dd89096.PNG)

* Running Azure App Service from Azure Pipelines automatic deployment

![Azure_pipelines_build](https://user-images.githubusercontent.com/92888738/149522029-1da71e1b-5248-4b85-935c-609b4830f10d.PNG)

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

![make_prediction](https://user-images.githubusercontent.com/92888738/148789414-d1dc4941-d95a-4cf5-8437-365cc6064a50.PNG)

* Output of streamed log files from deployed application

![logs](https://user-images.githubusercontent.com/92888738/149523550-d054599b-955f-4129-95f9-26a1628b846b.PNG)

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


