# Teste Backend 2


# Teste Técnico Golang

## Escopo do Projeto

Desenvolver uma API RESTful em Golang que gerencia as entidades **Organização** e **Usuário**, permitindo a associação de usuários a organizações. A API deve implementar as operações CRUD para ambas as entidades e incluir endpoints para adicionar e remover usuários de uma organização. A arquitetura Clean Architecture será utilizada, juntamente com PostgreSQL como banco de dados, Redis para cache e Docker Compose para containerização. A autenticação JWT será implementada para garantir a segurança da API.

## Requisitos Técnicos

- **Linguagem:** Golang
- **Arquitetura:** Clean Architecture
- **Banco de Dados:** PostgreSQL (sem ORM)
- **Cache:** Redis
- **Containerização:** Docker Compose
- **Autenticação:** JWT
- **Framework Web (opcional):** Escolha sua biblioteca preferida (ex: Gin, Echo, Fiber)

## Entidades

- **Organização:**
    - ID
    - Nome
    - Documento
- **Usuário:**
    - ID
    - Nome
    - Email
    - Telefone
    - Documento

## Endpoints da API

**Organizações:**

- `POST /api/organizations`: Criar uma nova organização.
- `GET /api/organizations`: Listar todas as organizações.
- `GET /api/organizations/{id}`: Obter uma organização por ID.
- `PUT /api/organizations/{id}`: Atualizar uma organização.
- `DELETE /api/organizations/{id}`: Deletar uma organização.

**Usuários:**

- `POST /api/users`: Criar um novo usuário.
- `GET /api/users`: Listar todos os usuários.
- `GET /api/users/{id}`: Obter um usuário por ID.
- `PUT /api/users/{id}`: Atualizar um usuário.
- `DELETE /api/users/{id}`: Deletar um usuário.

**Associação Organização-Usuário:**

- `POST /api/organizations/{orgId}/users/{userId}`: Adicionar um usuário a uma organização.
- `DELETE /api/organizations/{orgId}/users/{userId}`: Remover um usuário de uma organização.

**Autenticação:**

- `POST /api/login`: Obter um token JWT fornecendo email e senha válidos.

## Instruções

1. **Crie um repositório no GitHub:** Nomeie o repositório como "go-clean-arch-org-user-api".
2. **Estruture o projeto:** Organize o código seguindo os princípios da Clean Architecture.
3. **Implemente a API:**
    - Utilize o framework web de sua preferência ou as bibliotecas padrão do Golang.
    - Escreva queries SQL otimizadas para interagir com o PostgreSQL.
    - Implemente a autenticação JWT e proteja os endpoints necessários.
    - Utilize o Redis para armazenar em cache os resultados de consultas frequentes.
4. **Crie o Docker Compose:** Defina os serviços para PostgreSQL, Redis e a API Golang.
5. **Documente o projeto:** Crie um arquivo README.md detalhado.

## Avaliação

A avaliação seguirá os critérios mencionados anteriormente, com ênfase na otimização das queries SQL e na implementação da autenticação JWT.

## Prazo de Entrega

O prazo de entrega é de **7 dias**.

## Observações

- Utilize as melhores práticas de segurança ao implementar a autenticação JWT.
- Ao escrever as queries SQL, considere a performance e a escalabilidade da aplicação.
- Sinta-se à vontade para utilizar bibliotecas adicionais para auxiliar na implementação do JWT e na conexão com o Redis.
- Em caso de dúvidas, não hesite em perguntar.
