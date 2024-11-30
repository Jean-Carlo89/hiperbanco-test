
# Guia para Executar o Projeto

## 1. Rodar por Docker

### Comando para subir as instâncias:
```bash
docker compose up ou docker-compose up a depender da versão instalada
```


> Este comando subirá as instâncias do Redis, MySQL e a aplicação.

### Configurações Padrão:
- **Redis:** Porta `6379`
- **MySQL:** Porta `3306`
- **App:** Porta `3000`

### Arquivos de Configuração:
- As configurações de ambiente para produção estão definidas no arquivo `.env.prod`.

### Testes Rápidos:
- Há um arquivo `api.http` incluído no projeto para facilitar testes rápidos dos endpoints.


> Para utilizar o arquivo `api.http` no VS Code, é necessário instalar a extensão [Rest Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client).

### Ferramentas Alternativas:
- Você pode utilizar o **Postman** ou qualquer outra ferramenta similar para testar os endpoints.

---

## 2. Executar Localmente

### Comando para rodar o app localmente:
```bash
npm run dev
```

**Comentário:**
> Para evitar a necessidade de instalar o MySQL e Redis localmente, é recomendado subir os containers com o comando anterior do Docker Compose antes de executar a aplicação localmente. 

### Recomendações:
- Suba os serviços necessários com o comando:
  ```bash
  docker compose up db redis
  ```

- A aplicação rodará na porta `3001` quando executada localmente.
- As configurações de ambiente para desenvolvimento estão no arquivo `.env.dev`.

---

## 3. Estrutura do Projeto

**Comentário:**
> Procurei seguir os exemplos dados para moldar as respostas e estrutura do projeto.

- As implementações de **Consumers** e **Producers** foram feitas seguindo os exemplos disponibilizados na documentação oficial de **Queues do Nest.js**.

---

## 4. Testes Rápidos

### Arquivo `api.http`:
O projeto inclui o arquivo `api.http`, que permite realizar testes rápidos dos endpoints.

### Requisitos:
- **VS Code** com a extensão [Rest Client](https://marketplace.visualstudio.com/items?itemName=humao.rest-client).

**Comentário:**
> Este arquivo facilita a realização de requisições HTTP diretamente pelo editor de código.

### Como Usar:
1. Abra o arquivo `api.http` no **VS Code**.
2. Clique na opção `Send Request` ao lado das requisições no arquivo para executá-las.

---

## 5. Ferramentas Alternativas para Teste

Além do `api.http`, você pode testar os endpoints utilizando:
- **Postman**
- **Insomnia**
- **Qualquer outra ferramenta de requisições HTTP**

---
