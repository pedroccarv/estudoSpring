# ☕ Spring Boot Course Project

[![Java](https://img.shields.io/badge/Java-21-orange.svg)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-blue.svg)](https://www.postgresql.org/)

## 💻 Sobre o Projeto

Este é um projeto desenvolvido para fins de estudo, focado na construção de uma API RESTful utilizando o ecossistema **Spring Boot**.

O objetivo principal foi praticar a arquitetura em camadas, injeção de dependência, tratamento de exceções e persistência de dados com JPA/Hibernate.

## ⚙️ Arquitetura

O projeto segue a estrutura padrão de camadas do Spring:

* **config**: Configurações do projeto (ex: instanciação de banco de dados de teste).
* **resources**: Camada de controladores REST (Web Layer).
* **services**: Camada de serviço (lógica de negócio).
* **repositories**: Camada de acesso a dados (Data Access Layer).
* **entities**: Entidades do domínio (JPA).

## 🛠 Tecnologias Utilizadas

* **Java 21**
* **Spring Boot**
* **Spring Data JPA** (Hibernate)
* **Banco de Dados H2** (para ambiente de Teste/Desenvolvimento)
* **PostgreSQL** (para ambiente de Produção)
* **Maven** (Gerenciamento de dependências)

## 🚀 Como executar o projeto

### Pré-requisitos
* Java 21 instalado
* Maven instalado

### Passos
1.  Clone o repositório:
    ```bash
    git clone https://github.com/pedroccarv/estudoSpring.git
    ```
2.  Entre na pasta do projeto:
    ```bash
    cd course
    ```
3.  Execute a aplicação:
    ```bash
    mvn spring-boot:run
    ```

> **Nota:** Por padrão, o projeto pode estar configurado para usar o banco de dados H2 (em memória). Para acessar o console do H2, inicie a aplicação e acesse: `http://localhost:8080/h2-console`.

## endpoints 🔌 Endpoints da API

Abaixo estão os principais recursos disponíveis na API, baseados nas entidades do domínio:

| Recurso | Método | Endpoint | Descrição |
|---|---|---|---|
| **Usuários** | GET | `/users` | Lista todos os usuários |
| | GET | `/users/{id}` | Busca um usuário por ID |
| **Pedidos** | GET | `/orders` | Lista todos os pedidos realizados |
| | GET | `/orders/{id}` | Busca detalhes de um pedido específico |
| **Categorias** | GET | `/categories` | Lista as categorias de produtos |
| **Produtos** | GET | `/products` | Lista os produtos disponíveis |

> **Nota:** A API também gerencia entidades dependentes como `Payment` e `OrderItem` através das operações de Pedido.

## 📦 Estrutura de Banco de Dados

O projeto está configurado para trabalhar com dois perfis de banco de dados:
1.  **Test Profile**: Utiliza o H2 Database para testes rápidos e seeding de dados.
2.  **Dev/Prod Profile**: Configurado para conectar ao PostgreSQL.

## 👨‍💻 Autor

**Pedro**
* [LinkedIn](https://www.linkedin.com/in/pedrohcpereira/)
* [GitHub](https://github.com/pedroccarv)
