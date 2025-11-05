# ---- Build ----
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src


# copy csproj and restore as distinct layers
COPY src/SampleApi/SampleApi.csproj ./SampleApi/
RUN dotnet restore SampleApi/SampleApi.csproj


# copy everything else and publish
COPY src/ ./
WORKDIR /src/SampleApi
RUN dotnet publish -c Release -o /app/publish --no-restore


# ---- Runtime ----
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS runtime
WORKDIR /app
COPY --from=build /app/publish ./


# Use environment variables for configuration (example defaults)
ENV ASPNETCORE_URLS="http://+:8080"
ENV ASPNETCORE_ENVIRONMENT=Production


EXPOSE 8080
ENTRYPOINT ["dotnet", "SampleApi.dll"]