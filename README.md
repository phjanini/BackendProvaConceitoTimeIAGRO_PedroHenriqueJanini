# Catálogo de Livros - API REST

API RESTful desenvolvida em .NET Core para gerenciamento de catálogo de livros, permitindo busca, ordenação e cálculo de frete.

## 📋 Sobre o Projeto

Este projeto é a solução de um teste desenvolvido como parte do processo seletivo para Desenvolvedor C#. A API permite:

- ✅ Buscar livros em um catálogo JSON
- ✅ Filtrar livros por especificações (autor, nome, gênero, etc.)
- ✅ Ordenar resultados por preço (ascendente e descendente)
- ✅ Calcular valor do frete (20% do valor do livro)

## 🏗️ Arquitetura do Projeto

O projeto foi estruturado em **3 camadas** seguindo princípios SOLID e boas práticas de desenvolvimento:

```
BackendProvaConceitoTimeIAGRO_PedroHenriqueJanini/
├── Hamurabi.Api/          # Camada de apresentação (Controllers e API)
├── Hamurabi.Core/         # Camada de negócio (Models, Interfaces, Services)
├── Hamurabi.Tests/        # Testes unitários
└── books.json             # Base de dados (arquivo JSON)
```

### Hamurabi.Core (Núcleo da Aplicação)
- **Models**: Classes que representam as entidades (Book, BookSpecifications)
- **Interfaces**: Contratos para Repository e Service
- **Services**: Lógica de negócio (busca, ordenação)
- **Repositories**: Acesso aos dados (leitura do JSON)

### Hamurabi.Api (Camada de API)
- **Controllers**: Endpoints REST
- **Program.cs**: Configuração da aplicação

### Hamurabi.Tests
- Testes unitários utilizando xUnit

## 🔧 Tecnologias Utilizadas

- **.NET 10.0** (compatível com .NET Core 3.1+)
- **ASP.NET Core Web API**
- **System.Text.Json** (para manipulação de JSON)
- **xUnit** (para testes unitários)

## 📦 Pré-requisitos

Para executar este projeto, você precisa ter instalado:

- [.NET SDK 6.0 ou superior](https://dotnet.microsoft.com/download)
- Visual Studio Code ou Visual Studio 2022

## 🚀 Como Executar o Projeto

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/BackendProvaConceitoTimeIAGRO_PedroHenriqueJanini.git
cd BackendProvaConceitoTimeIAGRO_PedroHenriqueJanini
```

### 2. Restaure as dependências

```bash
dotnet restore
```

### 3. Compile o projeto

```bash
dotnet build
```

### 4. Execute a API

```bash
cd Hamurabi.Api
dotnet run
```

A API estará disponível. Verifique no terminal a URL exibida (geralmente `http://localhost:5xxx`).

### 5. Acesse a documentação Swagger

Abra o navegador e acesse a URL `/swagger` mostrada no terminal, por exemplo:
```
http://localhost:5161/swagger
```

## 🧪 Como Executar os Testes

Para executar todos os testes unitários:

```bash
dotnet test
```

Para executar com detalhes:

```bash
dotnet test --logger "console;verbosity=detailed"
```

## 📚 Endpoints da API

(Em desenvolvimento - será atualizado conforme implementação dos Controllers)

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET | `/api/books` | Retorna todos os livros |
| GET | `/api/books/search?term={termo}` | Busca livros por termo |
| GET | `/api/books/ordered?ascending={true/false}` | Retorna livros ordenados por preço |
| GET | `/api/books/{id}/shipping` | Calcula frete de um livro |

## 🎯 Padrões de Projeto Utilizados

- **Repository Pattern**: Abstração da camada de acesso a dados
- **Dependency Injection**: Inversão de dependência e baixo acoplamento
- **Service Layer**: Separação da lógica de negócio
- **SOLID Principles**: Código organizado e manutenível

## 👤 Autor

**Pedro Henrique Janini**

Desenvolvido como prova de conceito para processo seletivo do time IAGRO.

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais e de avaliação técnica.

---

**Nota**: Este README será atualizado conforme o desenvolvimento do projeto avança.