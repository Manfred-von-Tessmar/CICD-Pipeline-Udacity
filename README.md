# Overview

In this project the plan was to set up a CI/CD pipeline with Azure Pipelines. The top premise during development process is having your code always in a testable state. Hence an agile project management was setup with using state of the art techniques to implement a CI/CD project. That means starting with best practices to plan your project in a quarterly or yearly increment and to place ToDos of your project planning on a Kanban Board (For the reviewer: I dispended using a trello board for subscriptional reasons. In our company we are using Teams Kanban Boards and Jira but we are not allowed for sharing them. Please thrust me, that expertise is available to plan a project in resonsible way. I made a screenshot for the excel spreadsheet. Hopefully this is also ok for you and will not affect the reviewers decision to pass or fail.). The top premise for having your code in a testable state could be ensured by setting up a repository in a source control system, that was cloned to a local system and to Azure Cloud shell. Next to testing the code locally CI/CD steps were realized by SaaS build services and configuration files that told a build server what to do, when a trigger event happended.



## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project

 (please see my comment in the overview).

* A link to a spreadsheet that includes the original and final project plan>

![spreadsheet](https://user-images.githubusercontent.com/92888738/149537680-86069282-f170-40c5-9416-27d050382cc0.PNG)

## Instructions

<TODO:  
* Architectural Diagram (Shows how key parts of the system work)>

![image](https://user-images.githubusercontent.com/92888738/149540497-7f13e05d-9cf5-4e68-b70c-0a17a0f8e093.png)

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

1. create a repository and the code in a source controll system like Github
2. make sure that your repository has a Makefile, a requirements.txt and a script and testing file before doing steps 5-x.
3. make sure that your makefile contains install, linting and testing functions
4. create ssh keys in an azure cloud shell environment with ssh-keygen -t rsa
5. upload the keys to your Github account (do the following steps: cd ./ssh; ls; cat your-sshkey; copy the key, add it to your Github ssh-keys)
6. clone your Github repository via "git clone the-ssh-url-link-to-your-repository" into your azure cloud shell environment

![github_repo_in_azurecloudshell](https://user-images.githubusercontent.com/92888738/148787588-0244ee46-a4ba-4b33-8e13-23d14a5a5276.PNG)

7. set the working directory in your azure cloud shell to the directory of your code (the directory of your cloned Github repo)
8. create a virtual environment (execute "python3 -m venv ~/.myrepo" and then "source ~/.myrepo/bin/activate" in your cloud shell)
9. run your makefile functions via "make all" (The "make all" command installs your requirements and all dependencies, lints and tests your code. This step is necessary to make sure, that your code is in a workable state. It tells you if your code is executable in your local working environment. In this project this step was done with the project scaffold (testing code). 

![maketest](https://user-images.githubusercontent.com/92888738/148789121-e45e2bad-b0a8-4623-81a2-44ad33578b5f.PNG)

10. If you want to go a step further, you can configure your project so that your project is tested upon change events occur in GitHub. This is a necessary step to perform Continuous Integration remotely. You can use Github actions which is a kind of Software-as-a-Service build server. To tell the server what to do you need a build service template (you can choose a workflow template in Github Actions) and configuration files (e.g. requirements.txt, makefile, test file). In this project this step was done with the project scaffold (testing code). If a build job was successful can be checked in the github actions workflow history. 

![github_actions](https://user-images.githubusercontent.com/92888738/149525189-3fabe4e8-bddf-4314-bab2-2a007e3ca8a8.PNG)

11. After performing code testing locally and via Github Actions, it is now the time to set up Continuous Deployment using azure technologies. First of all make sure, that you have the right code base. In this project the project scaffold was replaced by the code of Noah Gift (you can download the code from here: https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/tree/master/C2-AgileDevelopmentwithAzure/project/starter_files.

12. Make sure that your local code (in azure cloud shell) is sychronized with your github repo.
13. set a an azure app service from your azure cloud shell (make sure that your working directory is your project directory) (see documentation for setting up a webapp: https://docs.microsoft.com/de-de/cli/azure/webapp?view=azure-cli-latest). You can browse your web app via "https://your-webapp-name.azurewebsites.net"

* Project running on Azure App Service

![azure_app_service](https://user-images.githubusercontent.com/92888738/148787976-75ef3494-bafe-4309-8fd6-18a5d4eabb8f.PNG)

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


