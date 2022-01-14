# Overview

In this project the plan was to set up a CI/CD pipeline with Azure Pipelines. The top premise during development process is having your code always in a testable state. Hence an agile project management was setup with using state of the art techniques to implement a CI/CD project. That means starting with best practices to plan your project in a quarterly or yearly increment and to place ToDos of your project planning on a Kanban Board (For the reviewer: I dispended using a trello board for subscriptional reasons. In our company we are using Teams Kanban Boards and Jira but we are not allowed for sharing them. Please thrust me, that expertise is available to plan a project in resonsible way. I made a screenshot for the excel spreadsheet. Hopefully this is also ok for you and will not affect the reviewers decision to pass or fail.). The top premise for having your code in a testable state could be ensured by setting up a repository in a source control system, that was cloned to a local system and to Azure Cloud shell. Next to testing the code locally CI/CD steps were realized by SaaS build services and configuration files that told a build server what to do, when a trigger event happended.



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

 ![github_actions](https://user-images.githubusercontent.com/92888738/149525189-3fabe4e8-bddf-4314-bab2-2a007e3ca8a8.PNG)

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


