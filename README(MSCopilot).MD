markdown
# MegaMan Bosses API

Este é um projeto de uma API desenvolvida em .NET Core 3.1 para listar os dados dos bosses do jogo MegaMan. O principal objetivo é fornecer um backend que retorna informações em JSON sobre cada boss no formato especificado.

## Estrutura JSON

A API fornece dados no seguinte formato JSON:

```json
{
  "Id": 1,
  "Code": "DLN/DRN-003",
  "Name": "Cutman",
  "HP": 150,
  "Picture": "https://vignette.wikia.nocookie.net/megaman/images/2/22/Cutman.png"
}
Especificações do Projeto
SDK Utilizado
xml
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
Dependências
O projeto utiliza os seguintes pacotes NuGet:

Microsoft.EntityFrameworkCore versão 3.1.8

Microsoft.EntityFrameworkCore.Design versão 3.1.8

Microsoft.EntityFrameworkCore.SqlServer versão 3.1.8

Newtonsoft.Json versão 12.0.2

Como Executar
Clone o repositório para sua máquina local.

Navegue até o diretório do projeto.

Restaure as dependências do projeto utilizando dotnet restore.

Execute a aplicação utilizando dotnet run.

Endpoints Disponíveis
Método HTTP	Endpoint	Descrição
GET	/api/bosses	Retorna a lista de todos os bosses
GET	/api/bosses/{id}	Retorna os dados de um boss específico
Contribuindo
Se você deseja contribuir com este projeto, por favor, siga os passos abaixo:

Faça um fork deste repositório.

Crie uma branch para sua feature (git checkout -b feature/nova-feature).

Commit suas mudanças (git commit -m 'Adiciona nova feature').

Envie suas mudanças (git push origin feature/nova-feature).

Abra um Pull Request.

Licença
Este projeto está licenciado sob a licença MIT - veja o arquivo LICENSE para mais detalhes.

Contato
Caso tenha alguma dúvida ou sugestão, sinta-se à vontade para entrar em contato.
