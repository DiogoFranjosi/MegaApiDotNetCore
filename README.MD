<h1 align="center">
  <br />
  <img
    src="./_docs/assets/icon.png"
    alt="Mega Man Robots API"
    width="150"
  />
  <br />
  <b>Mega Man Robots API</b>
  <br />
  <sub
    ><sup><b>(MEGA-MAN-ROBOTS)</b></sup></sub
  >
  <br />
  <a
    href="https://github.com/DiogoFranjosi/MegaApiDotnetCore/actions/workflows/build.yml"
  >
    <img
      src="https://github.com/DiogoFranjosi/MegaApiDotnetCore/actions/workflows/build.yml/badge.svg"
      alt=""
    />
  </a>
  <a href="https://github.com/DiogoFranjosi/MegaApiDotnetCore/releases/latest">
    <img
      src="https://img.shields.io/github/v/release/DiogoFranjosi/MegaApiDotnetCore"
      alt="Latest Release"
    />
  </a>
</h1>

<p align="center">
  Esta API desenvolvida em .NET Core 3.1 lista os dados dos bosses da franquia Mega Man. O objetivo é fornecer um backend que retorna informações sobre os robôs.
  <br />
</p>

<p align="cente

<p align="center">
  <br />
  <img src="./_docs/assets/carbon.png" />
</p>

## Tecnologias Utilizadas

- **ASP.NET Core 3.1** - Estrutura principal do backend
- **Entity Framework Core** - ORM para interação com o banco de dados
- **Newtonsoft.Json** - Manipulação de JSON


## Dependências Utilizadas

A API utiliza as seguintes dependências:

| Dependência | Versão | Link |
|-------------|---------|------|
| Microsoft.EntityFrameworkCore | 3.1.8 | [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/) |
| Microsoft.EntityFrameworkCore.Design | 3.1.8 | [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/) |
| Microsoft.EntityFrameworkCore.SqlServer | 3.1.8 | [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/) |
| Newtonsoft.Json | 12.0.2 | [NuGet](https://www.nuget.org/packages/Newtonsoft.Json/) |

## Endpoints da API

| Método | Endpoint | Descrição |
|--------|---------|------------|
| **GET** | `/api/v1/robots` | Lista todos os robôs |
| **GET** | `/api/v1/robots/{id}` | Busca um robô pelo ID |
| **POST** | `/api/v1/robots` | Cria um novo robô |

## Técnicas Utilizadas

- **Arquitetura em Camadas** - Separação do código em Controllers, Services e Models.
- **Injeção de Dependência** - Utilização de `IRobotServices` para facilitar testes e modularidade.
- **RESTful API** - Padrão para comunicação baseada em HTTP.
- **Tratamento de Erros** - Retorno adequado de códigos HTTP (`200 OK`, `404 Not Found`).

## Configuração e Execução

1. Clone o repositório:
   ```sh
   git clone https://github.com/seu-usuario/megaman-api.git
   ```
2. Navegue até o diretório do projeto:
   ```sh
   cd megaman-api
   ```
3. Restaure as dependências:
   ```sh
   dotnet restore
   ```
4. Execute o projeto:
   ```sh
   dotnet run
   ```

## Arquitetura

```🌐
src
├── 📂 Controllers      [Routes for endpoints]
├── 📂 Models           [Database models]
├── 📂 Services         [Business rules]
├── 📂 Middlewares      [Intermediate functions between the HTTP request and the final server response]
├── 📂 Database         [Structures related to the database]
│   ├── 📂 DTOs             [Input Models and View Models (Data Transfer Objects)]
│   ├── 📂 EntityFramework  [Files related to the ORM Entity Framework]
│   │     ├── 📂 Context         [Entity context settings]
│   │     ├── 📂 Migrations      [Migrations for database updates]
│   ├── 📂 Repositories     [Repository pattern]
```

## Autor

 Desenvolvido por Diogo Franjosi - [Github](https://github.com/DiogoFranjosi)

