#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompat

FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-nanoserver-1809 AS base

COPY . /app
WORKDIR /app
ENTRYPOINT ["dotnet", "TestDeployment.dll"]
#EXPOSE 80
#EXPOSE 443

#FROM mcr.microsoft.com/dotnet/core/sdk:2.2-nanoserver-1809 AS build
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