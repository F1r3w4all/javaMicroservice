#  Receita MicroService

Este projeto é um **microsserviço de gerenciamento de receitas** desenvolvido em **Java** com **Spring Boot** e banco de dados **MongoDB Atlas**.  
Ele faz parte de uma arquitetura baseada em **microsserviços**, podendo se integrar a outros serviços como usuários, planos alimentares e frontend em React/Next.js.

---

##  Funcionalidades

-  Cadastro de receitas
-  Consulta de receitas
-  Atualização de receitas
-  Exclusão de receitas
-  Integração via API REST

---

##  Estrutura do Projeto

receitaMicroService/
│── src/main/java/com/receita/
│   ├── controller/    # Controladores REST (endpoints)
│   ├── model/         # Modelos de dados (Receita, Ingrediente, etc.)
│   ├── repository/    # Interfaces do MongoDB (Spring Data)
│   ├── service/       # Regras de negócio
│   └── ReceitaApp.java# Classe principal Spring Boot
│── src/main/resources/
│   ├── application.properties  # Configurações do Spring Boot
│── pom.xml            # Dependências e build Maven

---

##  Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot 3+**
- **Spring Data MongoDB**
- **MongoDB Atlas (cloud database)**
- **Maven** (gerenciamento de dependências)

---

##  Configuração

No arquivo src/main/resources/application.properties, configure sua conexão com o MongoDB Atlas:

spring.data.mongodb.uri=mongodb+srv://<usuario>:<senha>@<cluster>.mongodb.net/<database>
spring.data.mongodb.database=receitas
server.port=8081

---

##  Como Executar

1. **Clone o repositório**
   git clone https://github.com/seu-usuario/receitaMicroService.git
   cd receitaMicroService

2. **Compile e execute com Maven**
   mvn clean install
   mvn spring-boot:run

3. **Acesse a API**
   Base URL: http://localhost:8081/api/receitas

---

##  Endpoints Principais

| Método | Endpoint             | Descrição                  |
|--------|----------------------|----------------------------|
| GET    | /api/receitas        | Lista todas as receitas    |
| GET    | /api/receitas/{id}   | Busca uma receita por ID   |
| POST   | /api/receitas        | Cria uma nova receita      |
| PUT    | /api/receitas/{id}   | Atualiza uma receita       |
| DELETE | /api/receitas/{id}   | Remove uma receita         |




---

## 👨‍💻 Autor

Desenvolvido por **Ulisses Magalhães**
