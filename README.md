# Overview

In this project the plan was to set up a CI/CD pipeline with Azure Pipelines. The top premise during development process is having your code always in a testable state. Hence an agile project management was setup with using state of the art techniques to implement a CI/CD project. That means starting with best practices to plan your project in a quarterly or yearly increment and to place ToDos of your project planning on a Kanban Board. The top premise for having your code in a testable state could be ensured by setting up a repository in a source control system, that was cloned to a local system and to Azure Cloud shell. Next to testing the code locally CI/CD steps were realized by SaaS build services and configuration files that told a build server what to do, when a trigger event happended.



## Project Plan

https://docs.google.com/spreadsheets/d/1-_3-LWYUVAqNGMI3vqqHc-ZrG-742vIwFIEWMG5z4Hs/edit?usp=drivesdk
https://trello.com/b/EAQC8KmM/udacity-cicd-pipeline


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

![example workflow](https://github.com/Manfred-von-Tessmar/CICD-Pipeline-Udacity/actions/workflows/python-app.yml/badge.svg)
(since the python-app.yml was replaced by azure-pipelines.yml, the test is failing, the picture above shows successful runs with python-app.yml build)

11. After performing code testing locally and via Github Actions, it is now the time to set up Continuous Deployment using azure technologies. First of all make sure, that you have the right code base. In this project the project scaffold was replaced by the code of Noah Gift (you can download the code from here: https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/tree/master/C2-AgileDevelopmentwithAzure/project/starter_files.

12. Make sure that your local code (in azure cloud shell) is sychronized with your github repo.
13. set a an azure app service from your azure cloud shell (make sure that your working directory is your project directory) (see documentation for setting up a webapp: https://docs.microsoft.com/de-de/cli/azure/webapp?view=azure-cli-latest). You can browse your web app via "https://your-webapp-name.azurewebsites.net"

![azure_app_service](https://user-images.githubusercontent.com/92888738/148787976-75ef3494-bafe-4309-8fd6-18a5d4eabb8f.PNG)

14. It is now the time for Continous Deployment of your project to your azure web applicaton. Therefore we want to use azure pipelines. What you need to do is creating a new project in Azure DevOps. To tell Azure Pipelines where the code is, you need to connect your Github Repo to Azure Pipelines (see documentation: https://docs.microsoft.com/de-de/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops&WT.mc_id=udacity_learn-wwl). In this case we want to use a CI/CD azure pipeline to provide the a python-web-app in Azure app service for Linux. When your Github Repository connection to Azure Pipelines was successfull and you have chosen the right build workflow in Azure Pipelines, a yml file named azure-pipelines.yml is created in your github repo. Your azure pipeline is ready for the first build.

You can see the build status of your build service in Azure pipelines.

![implement_pipelines_to_azure](https://user-images.githubusercontent.com/92888738/149521983-0c01a940-7820-48e5-814d-cd832dd89096.PNG)

15. You can see the build status of your build service in Azure pipelines.

![Azure_pipelines_build](https://user-images.githubusercontent.com/92888738/149522029-1da71e1b-5248-4b85-935c-609b4830f10d.PNG)

16. When your App is running you can do predictions from your Azure Cloud shell environment

![make_prediction](https://user-images.githubusercontent.com/92888738/148789414-d1dc4941-d95a-4cf5-8437-365cc6064a50.PNG)

17. The log entries for your web application can be checked with the following URL: your-web-app.scm.azurewebsites.net/ape/logs/docker

![logs](https://user-images.githubusercontent.com/92888738/149523550-d054599b-955f-4129-95f9-26a1628b846b.PNG)

## Enhancements

This project with its content and with the links to microsoft learning sites was a well balanced mixture of theory and practical parts and it led to much increased understanding for the CI/CD topic. I have no idea for enhancements. I Liked the content and how it was provided. Maybe in the final project on enhancement could be to more focus on the understanding for the code (maybe the student can write his own code, or should change the code so that the code is executable or what else). I didn`t like creating a trelloboard or a spreadsheet for the planning since it is a daily business and it needs time (I have a family with two children and I do the nanodegree program after work). So I would recommend omitting the trello board and the spreadsheet. The most understanding how a CI/CD pipeline worked, came from the content and the exercises itself. 

## Demo 

https://youtu.be/HtN1zdiCWl0


