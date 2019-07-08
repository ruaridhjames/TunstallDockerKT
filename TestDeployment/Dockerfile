#FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-stretch-slim AS base
#WORKDIR /app
#EXPOSE 80
#EXPOSE 443

#FROM mcr.microsoft.com/dotnet/core/sdk:2.2-stretch AS build
#WORKDIR /src
#COPY ["TestDeployment/TestDeployment.csproj", "TestDeployment/"]
#RUN dotnet restore "TestDeployment/TestDeployment.csproj"
#COPY . .
#WORKDIR "/src/TestDeployment"
#RUN dotnet build "TestDeployment.csproj" -c Release -o /app

#FROM build AS publish
#RUN dotnet publish "TestDeployment.csproj" -c Release -o /app

#FROM base AS final
#WORKDIR /app
#COPY --from=publish /app .
#ENTRYPOINT ["dotnet", "TestDeployment.dll"]

FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-nanoserver-1809 AS base

COPY . /app
WORKDIR /app
ENTRYPOINT ["dotnet", "TestDeployment.dll"]