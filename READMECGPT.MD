# MegaMan Bosses API

## Descrição
Este projeto é uma API desenvolvida em .NET Core 3.1 que fornece informações sobre os chefes (bosses) da franquia MegaMan. O objetivo principal é servir como um backend que disponibiliza dados no formato JSON.

## Exemplo de Resposta JSON
```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
```

## Tecnologias Utilizadas
- **.NET Core 3.1**
- **Entity Framework Core 3.1.8**
- **SQL Server**
- **Newtonsoft.Json 12.0.2**

## Estrutura do Projeto
O projeto utiliza o SDK Web do .NET e tem as seguintes dependências configuradas:
```xml
<Project Sdk="Microsoft.NET.Sdk.Web">

  <PropertyGroup>
    <TargetFramework>netcoreapp3.1</TargetFramework>
  </PropertyGroup>

  <ItemGroup>
    <PackageReference Include="Microsoft.EntityFrameworkCore" Version="3.1.8" />
    <PackageReference Include="Microsoft.EntityFrameworkCore.Design" Version="3.1.8">
      <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
      <PrivateAssets>all</PrivateAssets>
    </PackageReference>
    <PackageReference Include="Microsoft.EntityFrameworkCore.SqlServer" Version="3.1.8" />
    <PackageReference Include="Newtonsoft.Json" Version="12.0.2" />
  </ItemGroup>

</Project>
```

## Como Executar o Projeto
### Pré-requisitos
- .NET Core 3.1 SDK instalado
- SQL Server configurado

### Passos
1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-usuario/megaman-bosses-api.git
   ```
2. Navegue até a pasta do projeto:
   ```sh
   cd megaman-bosses-api
   ```
3. Restaure as dependências:
   ```sh
   dotnet restore
   ```
4. Configure a string de conexão com o banco de dados no arquivo `appsettings.json`.
5. Execute as migrações do banco de dados:
   ```sh
   dotnet ef database update
   ```
6. Inicie a API:
   ```sh
   dotnet run
   ```

A API estará disponível em `http://localhost:5000` por padrão.

## Endpoints
### Listar Todos os Bosses
- **GET** `/api/bosses`

### Obter um Boss Específico por ID
- **GET** `/api/bosses/{id}`

## Licença
Este projeto é de código aberto e está licenciado sob a licença MIT.
