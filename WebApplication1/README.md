# WebApplication1 – ASP.NET Core (.NET 8)

This project is a basic **.NET 8 Web Application** using Razor Pages. It demonstrates how to dockerize a .NET application using a `Dockerfile` and `docker-compose`.

## Tech Stack
- Docker

## Project Structure
WebApplication1
├── Dockerfile
├── WebApplication1
├── WebApplication1.sln
└── docker-compose.yaml

## Installation

### Prerequisites
- [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)



### Steps to Run Application using Docker Containers 




## **1. Clone the repository**

```sh
git clone https://github.com/vyawahareakash2210/Assignment_POC.git
cd Assignment_POC
cd WebApplication1/

```
## **2. Build the Docker image & Run the application using Docker Compose**

```sh
#docker-compose up --build -d
```

![alt text](image.png)


## **3. Check Running Docker Containers**

```sh
#docker ps

```

![alt text](image-2.png)


## **4. Access Running Docker Containers**

```sh
#http://localhost:8080

```

![alt text](image-1.png)


## **5. Access Running MySQL Containers**

```sh
#docker exec -it mysqldb bash
#mysql -u akash -p
#SHOW DATABASES;

```

![alt text](image-3.png)

## **6. Check Web App Container Logs**

```sh
#docker logs $containerID

```

![alt text](image-4.png)