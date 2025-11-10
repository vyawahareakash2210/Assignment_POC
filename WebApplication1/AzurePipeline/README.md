# Assignment: Dockerize a .NET 8 Application With CICD Pipeline and Deploy on Azure WebApp 

This project is a file containes details of  **Dockerize a .NET 8 Application With CICD Pipeline and Deploy on Azure WebApp ** 

## Overview

This Project Contains  below Tools  :
- Azure Devops YAML Pipeline  =  CICD
- Azure  Container registry = Docker Image Store 
- Azure Web App = Deploy Application on Azure 


### Stages  to Deloy  Application using Azure Pipeline  

1) Build   - Build Dotnet Application 
2) Publish   - Publish Artifact 
3) Docker_BuildAndPush  - Create Docker Image and Push it to  Azure  Container registry
4) DeployAppService  - Deploy Application on Azure Web App 



## **Stages in Pipeline**

![alt text](image.png)


## **Task Details  in Pipeline**

## **1) Dotnet_Build**

![alt text](image-1.png)


## **2) Dotnet_Publish**

![alt text](image-2.png)


## **3) Docker_BuildAndPush**

![alt text](image-3.png)

## **4) DeployAppService**

![alt text](image-4.png)


## **  Environment variables **

![alt text](image-6.png)

###  Application Running on  Azure WebApp Default domain
  

![alt text](image-5.png)


## **  Web App  Log stream for Container Platform  **

![alt text](image-7.png)


## **  Web App  Log stream for Web App Runtime  **


![alt text](image-8.png)