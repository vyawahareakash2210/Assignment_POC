# WebApplication1 – ASP.NET Core (.NET 8)

This project is a basic **.NET 8 Web Application** using Razor Pages. It demonstrates how to dockerize a .NET application using a `Dockerfile` and `docker-compose`.

## Tech Stack
- .NET 8
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

### Steps
1. Clone the repository:

git clone https://github.com/vyawahareakash2210/Assignment_POC.git
cd Assignment_POC
cd WebApplication1/

2.Build the Docker image & Run the application using Docker Compose :

docker-compose up --build -d

![alt text](image.png)

3. Check Running Docker Containers : 

 docker ps
![alt text](image-2.png)

3.Open your browser and navigate to:

http://localhost:8080

![alt text](image-1.png)

4. Access MySQL & Show Databases

docker exec -it mysqldb bash
mysql -u akash -p
SHOW DATABASES;


![alt text](image-3.png)


5. Web App Container Logs 

 docker logs #containerID

![alt text](image-4.png)