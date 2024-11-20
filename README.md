# 📚 **Bookstore**  

Bem-vindo ao **Bookstore**, um projeto desenvolvido para demonstrar fundamentos de **Programação Orientada a Objetos (POO)** em JavaScript.  
Este sistema simula uma livraria para venda de livros e pôsteres, aplicando conceitos como **classes**, **herança**, **polimorfismo**, **encapsulamento** e **abstração**.

---

## 🗂️ **Estrutura do Projeto**

A organização do projeto está dividida da seguinte forma:

```
BOOKSTORE/
├── entities/
│   ├── Author.js       // Representa os autores
│   ├── Book.js         // Representa os livros
│   ├── Order.js        // Representa os pedidos
│   ├── Poster.js       // Representa os pôsteres
│   ├── Product.js      // Classe base para todos os produtos
│   ├── Users.js        // Representa os usuários do sistema
├── App.js              // Classe principal para gerenciar a aplicação
├── Database.js         // Simula o banco de dados da aplicação
├── index.js            // Arquivo de execução do sistema
```

---

## ✨ **Principais Funcionalidades**

### 🔹 **Usuários**
- Cadastrar novos usuários com **nome**, **e-mail** e **senha**.
- Consultar todos os usuários cadastrados.

### 🔹 **Autores**
- Adicionar autores com **nome**, **nacionalidade** e uma **biografia**.
- Listar todos os autores disponíveis.

### 🔹 **Produtos**
#### **Livros**
- Cadastrar livros com informações como **título**, **sinopse**, **gênero**, **número de páginas**, **preço**, **estoque** e o **autor associado**.
- Consultar todos os livros disponíveis.

#### **Pôsteres**
- Cadastrar pôsteres com **nome**, **descrição**, **altura**, **largura**, **preço** e **estoque**.
- Consultar todos os pôsteres disponíveis.

### 🔹 **Estoque**
- Adicionar unidades ao estoque de livros ou pôsteres.
- Gerenciar a quantidade de itens em estoque automaticamente ao criar pedidos.

### 🔹 **Pedidos**
- Criar pedidos associando um usuário a uma lista de itens (livros e/ou pôsteres) com suas respectivas quantidades.
- Verificar o estoque disponível antes de concluir o pedido.
- Calcular o valor total do pedido automaticamente.

### 🔹 **Banco de Dados Simulado**
- Exibir o estado atual do banco de dados, mostrando usuários, autores, produtos e pedidos.

---

## 🛠️ **Conceitos de POO no Projeto**

### 🔸 **Encapsulamento**
Os dados de classes como `Order` e `User` são protegidos por meio de **propriedades privadas** (prefixadas por `#`), permitindo acesso controlado por métodos.

### 🔸 **Herança**
A classe `Product` serve como base para as classes `Book` e `Poster`, promovendo **reuso de código** e consistência.

### 🔸 **Polimorfismo**
Métodos como `saveProduct` e `removeProductFromStock` permitem tratamento uniforme para diferentes tipos de produtos (livros e pôsteres).

### 🔸 **Abstração**
As classes representam entidades do mundo real (livros, pôsteres, usuários, autores, pedidos), facilitando o entendimento e uso do sistema.

---

## 🚀 **Como Executar o Projeto**

### **Pré-requisitos**
Certifique-se de que o [Node.js](https://nodejs.org/) está instalado em sua máquina.

### **Passos para executar**
1. Clone o repositório:
   ```bash
   git clone https://github.com/dmardoqueu/bookstore
   ```
2. Navegue até o diretório do projeto:
   ```bash
   cd bookstore
   ```
3. Execute o arquivo principal:
   ```bash
   node index.js
   ```

---

## 📝 **Exemplo de Uso**

### **1. Cadastro de Autor e Livro**
```javascript
app.createAuthor('J. K. Rowling', 'British', 'Autora da série Harry Potter');
const authors = app.getAuthors();

app.createBook('Harry Potter e a Pedra Filosofal', '...', 'fantasy', 223, authors[0], 'Livro incrível...', 29.99, 50);
```

### **2. Cadastro de Usuário e Criação de Pedido**
```javascript
app.createUser('João', 'joao@email.com', 'senha123');
const users = app.getUsers();

const items = [
    { product: books[0], quantity: 2 }
];
app.createOrder(items, users[0]);
```

### **3. Exibição do Banco de Dados**
```javascript
app.showDatabase();
```

---

## 💡 **Principais Objetivos**

Este projeto tem como objetivo:
- Praticar os fundamentos de **Programação Orientada a Objetos (POO)**.
- Demonstrar o uso de conceitos como **herança**, **polimorfismo**, **encapsulamento** e **abstração** em um cenário prático.
- Simular o funcionamento básico de um sistema de gerenciamento de loja virtual.

---

Made by @dmardoqueu
