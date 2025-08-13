<<<<<<< HEAD
# dio-azure-devops-api
Este projeto foi criado como parte do desafio da [DIO (Digital Innovation One)]
=======
# API para Deploy no Azure com CI/CD via Azure DevOps

Este repositório contém o código-fonte e os arquivos de configuração para uma API .NET simples, projetada para ser construída como um contêiner Docker e implantada na nuvem da Azure através de um pipeline de CI/CD no Azure DevOps.

Este projeto foi criado como parte do desafio da [DIO (Digital Innovation One)](https://www.dio.me/).

## 🎯 Objetivo

O objetivo principal é demonstrar um fluxo de trabalho completo de CI/CD (Integração Contínua e Entrega Contínua), incluindo:
- Versionamento de código com Git e GitHub.
- Containerização da aplicação .NET com Docker.
- Automação de build e push da imagem Docker para o Azure Container Registry (ACR).
- Configuração de um pipeline como código usando `azure-pipelines.yml`.

## 📂 Estrutura do Repositório

Abaixo está a árvore de diretórios do projeto, mostrando a organização dos arquivos.

```
.
├── APITempo
│   ├── Controllers
│   │   └── WeatherForecastController.cs
│   ├── Properties
│   │   └── launchSettings.json
│   ├── appsettings.json
│   ├── APITempo.csproj
│   ├── Dockerfile
│   ├── Program.cs
│   └── WeatherForecast.cs
├── .gitignore
├── azure-pipelines.yml
└── README.md
```

### Descrição dos Arquivos Principais

- **`APITempo/`**: Pasta raiz do projeto .NET.
- **`Dockerfile`**: Define a receita para construir a imagem Docker da API. Utiliza um build multi-stage para otimização.
- **`azure-pipelines.yml`**: Arquivo de definição do pipeline "como código" para o Azure DevOps. Automatiza os passos de build e push da imagem.
- **`README.md`**: Esta documentação.

## 🚀 Como Usar

1.  **Clone o Repositório**: `git clone https://github.com/filisteus/dio-azure-devops-api.git`
2.  **Configure o Azure DevOps**:
    * Crie um novo projeto no Azure DevOps.
    * Crie um novo pipeline, selecionando "GitHub" e este repositório.
    * Configure as **Conexões de Serviço** (Service Connections) para sua assinatura do Azure e para o seu Azure Container Registry (ACR).
    * Atualize as variáveis no arquivo `azure-pipelines.yml` com os nomes das suas conexões, resource group e registry.
3.  **Execute o Pipeline**: O pipeline será acionado automaticamente a cada `push` na branch `main`.

## 👤 Autor

**Paulo Evaristo**
- **GitHub**: [filisteus](https://github.com/filisteus)
- **Email**: pevaristo@msn.com
>>>>>>> e093030 (feat: Initial project structure for Azure DevOps CI/CD)
