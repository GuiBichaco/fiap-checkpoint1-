# API de Pedidos

Esta API permite o gerenciamento de pedidos de clientes. Desenvolvida com **Spring Boot**, a API oferece operações de CRUD (Criar, Ler, Atualizar, Deletar) para gerenciar os pedidos em um banco de dados.

## Endpoints

A seguir estão os endpoints disponíveis para interagir com a API de pedidos:

### 1. Criar um novo pedido

- **Método:** `POST`
- **Endpoint:** `/pedidos`
- **Descrição:** Cria um novo pedido com o nome do cliente e o valor total.
  
**Exemplo de requisição:**
```json
{
  "clienteNome": "João Silva",
  "valorTotal": 150.50
}
```

**Exemplo de resposta:**
```json
{
  "id": 1,
  "clienteNome": "João Silva",
  "dataPedido": "2025-03-24",
  "valorTotal": 150.50
}
```

### 2. Buscar todos os pedidos

- **Método:** `GET`
- **Endpoint:** `/pedidos`
- **Descrição:** Retorna todos os pedidos registrados.

**Exemplo de resposta:**
```json
[
  {
    "id": 1,
    "clienteNome": "João Silva",
    "dataPedido": "2025-03-24",
    "valorTotal": 150.50
  },
  {
    "id": 2,
    "clienteNome": "Maria Oliveira",
    "dataPedido": "2025-03-25",
    "valorTotal": 200.00
  }
]
```

### 3. Buscar um pedido pelo ID

- **Método:** `GET`
- **Endpoint:** `/pedidos/{id}`
- **Descrição:** Retorna os detalhes de um pedido específico, identificando-o pelo ID.

**Exemplo de requisição:**
`GET /pedidos/1`

**Exemplo de resposta:**
```json
{
  "id": 1,
  "clienteNome": "João Silva",
  "dataPedido": "2025-03-24",
  "valorTotal": 150.50
}
```

### 4. Atualizar um pedido

- **Método:** `PUT`
- **Endpoint:** `/pedidos/{id}`
- **Descrição:** Atualiza um pedido existente, permitindo modificar o nome do cliente e o valor total do pedido.

**Exemplo de requisição:**
```json
{
  "clienteNome": "João Silva Atualizado",
  "valorTotal": 200.75
}
```

**Exemplo de resposta:**
```json
{
  "id": 1,
  "clienteNome": "João Silva Atualizado",
  "dataPedido": "2025-03-24",
  "valorTotal": 200.75
}
```

### 5. Deletar um pedido

- **Método:** `DELETE`
- **Endpoint:** `/pedidos/{id}`
- **Descrição:** Exclui um pedido do banco de dados com base no ID fornecido.

**Exemplo de requisição:**
`DELETE /pedidos/1`

**Exemplo de resposta:**
- **Status:** `204 No Content` (Não há conteúdo retornado na resposta)

---

## Como rodar o projeto

### Pré-requisitos

- JDK 17 ou superior
- Maven

### Passos para rodar a aplicação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/nome-do-repositorio.git
   ```

2. Acesse o diretório do projeto:
   ```bash
   cd nome-do-repositorio
   ```

3. Compile e execute o projeto utilizando Maven:
   ```bash
   mvn spring-boot:run
   ```

4. A API estará rodando em `http://localhost:8080`.

---

## Testes

Você pode testar os endpoints da API utilizando o [Postman](https://www.postman.com/) ou outra ferramenta semelhante. Utilize os exemplos de requisição e resposta descritos acima para testar as funcionalidades de criar, buscar, atualizar e excluir pedidos.

---

## Tecnologias Utilizadas

- **Spring Boot**: Framework para desenvolvimento de aplicações Java.
- **Spring Data JPA**: Para integração com bancos de dados relacionais.
- **H2 Database**: Banco de dados em memória para persistência de dados durante os testes.
- **Maven**: Gerenciador de dependências e construção do projeto.

---

## Contribuindo

Para contribuir com este projeto:

1. Faça um **fork** do repositório.
2. Crie uma **branch** para suas alterações (`git checkout -b minha-nova-feature`).
3. Faça **commit** das suas alterações (`git commit -am 'Adiciona nova feature'`).
4. Envie as alterações para o repositório remoto (`git push origin minha-nova-feature`).
5. Abra um **pull request**.

---

## Licença

Este projeto é licenciado sob a MIT License - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
```