# Stage 1: Build
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /app
COPY WebApplication1/*.csproj WebApplication1/
RUN dotnet restore WebApplication1/WebApplication1.csproj
COPY . .
RUN dotnet publish WebApplication1/WebApplication1.csproj -c Release -o /app/out

# Stage 2: Runtime
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime
WORKDIR /app
# Environment variables support
ENV ASPNETCORE_URLS=http://+:8080
ENV ASPNETCORE_ENVIRONMENT=Production

COPY --from=build /app/out .
EXPOSE 8080
ENTRYPOINT ["dotnet", "WebApplication1.dll"]
