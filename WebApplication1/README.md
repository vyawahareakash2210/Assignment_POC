# Assignment: Dockerize a .NET 8 Application

This project is a basic **.NET 8 Web Application** using Razor Pages. It demonstrates how to dockerize a .NET application using a `Dockerfile` and `docker-compose`.



## Overview

This Project Contains  below Files :
- WebApplication1
- Dockerfile
- docker-compose.yaml
- .dockerignore
- .env

## Tech Stack

```sh
- Docker

Web App Base Image : mcr.microsoft.com/dotnet/sdk:8.0
MySQL Base Image :   mysql:8.0


```




## Installation

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)



### Steps to Run Application using Docker Containers 


## **1. Clone the repository**

```sh
$ git clone https://github.com/vyawahareakash2210/Assignment_POC.git
$ cd Assignment_POC
$ cd WebApplication1/

```
## **2. Build the Docker image & Run the application using Docker Compose**

```sh
$ docker-compose up --build -d
```

![alt text](image.png)


## **3. Check Running Docker Containers**

```sh
$ docker ps

```

![alt text](image-2.png)


## **4. Access Running Docker Containers**

```sh
$ http://localhost:8080

```

![alt text](image-1.png)


## **5. Access Running MySQL Containers**

```sh

Access Database Container #mysqldb
$ docker exec -it mysqldb bash

connect to a MySQL database with user #Akash 

$ mysql -u akash -p

Enter Password as given in environment variables 

SHow Databases in MYSQL 

$ SHOW DATABASES;

```

![alt text](image-3.png)

## **6. Check Web App Container Logs**

```sh
$ docker logs $containerID

```

![alt text](image-4.png)







## ** Approach for Azure Deployment**

1) Prepare your Azure resources :
     1. Create an Azure Web App for Containers
         Runtime: Linux
         OS: Linux
         SKU: Choose a suitable plan (B1/B2 for dev/test)

     2. Create an Azure Container Registry (ACR)
         This is where your Docker image will be pushed.

2) Create Azure DevOps pipeline :

    Below Will be steps in Pipeline to Build and deploy 
      1.  task: UseDotNet@2    - This task will ensure that correct .NET SDK version is available on the build agent before compiling or running .NET applications

      2. Docker@2 - This task will Build and Push Docker image into ACR 

      3. AzureWebAppContainer@1 -   This task will Deploy to Azure Web App




