Projeto Web API

Este projeto é uma API simples construída com ASP.NET Core 8.0, que utiliza AutoMapper para mapeamento de objetos e Dapper para acessar um banco de dados. Ele foi projetado para fornecer dados de usuários, com o objetivo de aprender e aplicar práticas comuns de desenvolvimento de back-end em um projeto web API.
Tecnologias Utilizadas

    ASP.NET Core 8.0: Framework utilizado para criar a API.
    AutoMapper: Biblioteca para mapeamento de objetos entre as camadas.
    Dapper: Micro ORM para consulta de banco de dados.
    SQL Server: Banco de dados utilizado para armazenar informações de usuários.
    Swashbuckle (Swagger): Para gerar documentação interativa da API.

Estrutura do Projeto

A estrutura do projeto segue o padrão de uma Web API simples com a separação de responsabilidades entre as camadas:

ProjetoWebApi/                                                                                                                                                                                                  
├── ProjetoWebApi/                                                                                                                                                                                              
│   ├── Program.cs           # Configuração e inicialização da aplicação                                                                                                                                        
│   ├── Services/            # Contém interfaces e implementações de serviços                                                                                                                                   
│   │   ├── IUsuarioInterface.cs # Interface para serviço de usuários                                                                                                                                           
│   │   └── UsuarioService.cs   # Implementação do serviço de usuários                                                                                                                                          
│   ├── Dto/                 # Contém os Data Transfer Objects (DTOs)                                                                                                                                           
│   │   └── UsuarioListarDto.cs # DTO para listar usuários                                                                                                                                                      
│   └── Models/              # Contém os modelos de dados                                                                                                                                                       
│       └── Usuario.cs       # Modelo de usuário                                                                                                                                                                
└── ProjetoWebApi.csproj     # Arquivo de configuração do projeto                                                                                                                                               

Funcionalidades

    Listar usuários: Endpoint que retorna uma lista de usuários armazenados no banco de dados.
    Swagger: A documentação da API é gerada automaticamente usando o Swagger, que pode ser acessado quando a aplicação está em execução.

Requisitos

    .NET 8.0 SDK ou superior: Para compilar e executar o projeto.
    SQL Server: Banco de dados utilizado para persistência de dados.
    Visual Studio Code (ou qualquer editor de sua escolha) com suporte para C# e ASP.NET Core.

Instalação

1- Clone o repositório:
git clone https://github.com/PedroOliveira-dev/projetoWebApi.git
cd projetoWebApi

2- Instale as dependências: O projeto já contém as dependências definidas no arquivo .csproj, mas para garantir que todas as dependências estejam atualizadas, execute:
dotnet restore

3- Configure o banco de dados: Certifique-se de que o banco de dados SQL Server está configurado corretamente. O string de conexão é recuperado do arquivo de configuração appsettings.json, e é importante garantir que a string de conexão apontando para o seu banco de dados esteja correta.

Exemplo de string de conexão no appsettings.json:
{
    "ConnectionStrings": {
        "DefaultConnection": "Server=seu_servidor;Database=seu_banco;User Id=seu_usuario;Password=sua_senha;"
    }
}

4- Executando o Projeto: Após configurar a conexão com o banco de dados, execute o seguinte comando para rodar o projeto:
dotnet run

    A aplicação estará disponível no endereço https://localhost:5001 ou http://localhost:5000, dependendo da configuração de HTTPS.

Endpoints

Abaixo estão os endpoints disponíveis na API:

    GET /weatherforecast: Retorna uma previsão do tempo aleatória.

Swagger: Você também pode acessar a documentação interativa da API utilizando o Swagger. Quando a aplicação estiver em execução, acesse http://localhost:5000/swagger para visualizar os endpoints e testá-los.
Como Contribuir

Se você deseja contribuir com melhorias ou correções para este projeto, siga as etapas abaixo:

-Fork este repositório.
-Crie uma nova branch:
-git checkout -b minha-nova-feature

Faça suas alterações e commit:
git commit -am 'Adicionando uma nova feature'

-Push para a branch criada:
git push origin minha-nova-feature

Abra um Pull Request para revisão.






