# Baozi Store API

API REST desenvolvida para o trabalho de **Desenvolvimento Web Back-End** - Uninter.

## Descrição

Sistema simples de controle de clientes, produtos e pedidos da **Baozi Store** (loja de pãozinho chinês).

## Tecnologias

- Java 17
- Spring Boot 3.2.5
- Spring Data JPA
- Banco H2 (em memória) – pode ser trocado por MySQL
- Postman (para testes)

## Como executar

### Pré-requisitos
- JDK 17 ou superior
- Maven 3.8+

### Passos

```bash
# 1. Clone o repositório
git clone https://github.com/SEU_USUARIO/baozi-store-api.git
cd baozi-store-api

# 2. Execute a aplicação
./mvnw spring-boot:run
# ou
mvn spring-boot:run
```

A API estará disponível em: `http://localhost:8080`

Console H2 (opcional): `http://localhost:8080/h2-console`
- JDBC URL: `jdbc:h2:mem:baozistore`
- User: `sa`
- Password: (vazio)

## Endpoints

### Clientes (`/clientes`)
| Método | Endpoint          | Descrição          |
|--------|-------------------|--------------------|
| POST   | /clientes         | Criar cliente      |
| GET    | /clientes         | Listar todos       |
| GET    | /clientes/{id}    | Buscar por ID      |
| DELETE | /clientes/{id}    | Apagar             |
| PUT    | /clientes/{id}    | Atualizar (opcional)|

### Produtos (`/produtos`)
| Método | Endpoint          | Descrição          |
|--------|-------------------|--------------------|
| POST   | /produtos         | Criar produto      |
| GET    | /produtos         | Listar todos       |
| GET    | /produtos/{id}    | Buscar por ID      |
| DELETE | /produtos/{id}    | Apagar             |
| PUT    | /produtos/{id}    | Atualizar (opcional)|

### Pedidos (`/pedidos`)
| Método | Endpoint          | Descrição          |
|--------|-------------------|--------------------|
| POST   | /pedidos          | Criar pedido       |
| GET    | /pedidos          | Listar todos       |
| GET    | /pedidos/{id}     | Buscar por ID      |
| DELETE | /pedidos/{id}     | Apagar             |
| PUT    | /pedidos/{id}     | Atualizar (opcional)|

## Exemplos de JSON

### Criar Cliente
```json
{
  "nome": "JorgeLucas5566290",
  "clienteDesde": "2025-03-10"
}
```

### Criar Produto
```json
{
  "nome": "Baozi de Porco",
  "preco": 8.50,
  "estoque": true
}
```

### Criar Pedido
```json
{
  "clienteId": 1,
  "produtoId": 1,
  "quantidade": 5
}
```

## Autor

Jorge Lucas - RU 5566290  
Trabalho de Desenvolvimento Web Back-End - Uninter
