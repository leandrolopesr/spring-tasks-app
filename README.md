# ToDo List com Spring Boot

Este é um projeto de exemplo de uma aplicação de lista de tarefas (ToDo List) construída com o Spring Boot. Ele demonstra como criar uma aplicação Java web usando o Spring Boot, Spring Web, Spring Data JPA e Spring WebFlux.

## Requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas em seu ambiente de desenvolvimento:

- Java JDK 17 ou superior
- Maven (ou use o Wrapper fornecido)
- MySQL (ou outro banco de dados de sua escolha)

## Configuração do Banco de Dados

Este projeto usa o MySQL como banco de dados padrão. Você pode configurar as informações de conexão com o banco de dados no arquivo `src/main/resources/application.properties`.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/seu_banco_de_dados
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
```

## Executando a Aplicação
Você pode executar a aplicação usando o Maven:

```
mvn spring-boot:run
```
Acesse a aplicação no navegador em http://localhost:8080.

## Endpoints
- GET /todos: Retorna a lista de tarefas.
- POST /todos: Cria uma nova tarefa.
- GET /todos/{id}: Retorna os detalhes de uma tarefa específica.
- PUT /todos/{id}: Atualiza uma tarefa existente.
- DELETE /todos/{id}: Exclui uma tarefa.

## Dependências Principais

- **Spring Boot DevTools**  - O Spring Boot DevTools acelera o desenvolvimento com reinicialização automática e LiveReload.
- **Lombok** - biblioteca Java que reduz a verbosidade do código, gerando automaticamente getters, setters, construtores e outros métodos comuns por meio de anotações.
- **MySQL Driver** - Essa dependência é fundamental para acessar e manipular dados no banco de dados MySQL.
- **Validation (Bean Validation com Hibernate Validator)** - Nos permite definir regras de validação. Podemos garantir que os campos obrigatórios não estejam vazios e que as datas sejam válidas.
- **Spring Web** - Este módulo é usado para criar endpoints da web e controladores para manipular solicitações HTTP.
- **Spring Reactive Web** - Nos permite construir e testar nossos recursos de forma reativa, o que é uma vantagem, especialmente se desejamos escalá-lo no futuro ou lidar com tarefas em tempo real.
- **Spring Data JPA** - Esta dependência é usada para criar repositórios e acessar bancos de dados SQL com facilidade.
