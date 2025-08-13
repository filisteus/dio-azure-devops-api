# Estágio 1: Build da Aplicação
FROM mcr.microsoft.com/dotnet/sdk:8.0 AS build
WORKDIR /src
COPY ["APITempo/APITempo.csproj", "APITempo/"]
RUN dotnet restore "APITempo/APITempo.csproj"
COPY . .
WORKDIR "/src/APITempo"
RUN dotnet build "APITempo.csproj" -c Release -o /app/build

# Estágio 2: Publicação da Aplicação
FROM build AS publish
RUN dotnet publish "APITempo.csproj" -c Release -o /app/publish /p:UseAppHost=false

# Estágio 3: Imagem Final de Execução
FROM mcr.microsoft.com/dotnet/aspnet:8.0 AS final
WORKDIR /app
EXPOSE 8080
EXPOSE 8081
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "APITempo.dll"]
