FROM microsoft/aspnetcore-build:2.0 AS build-env

COPY . /app
WORKDIR /app
ENTRYPOINT ["dotnet", "TestDeployment.dll"]