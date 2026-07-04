# Biblioteca Online

## Integrantes

* Emilio Del Puppo Neto
* Fabrício Dansi
* Lohan Quintino

## Tema Escolhido

Biblioteca Online

## Descrição do Projeto

O projeto consiste em um sistema simples de gerenciamento de livros utilizando arquitetura Full Stack.

O Front-end foi desenvolvido com HTML, CSS e JavaScript, permitindo ao usuário cadastrar, listar, editar e excluir livros por meio de uma interface simples e intuitiva.

O Back-end foi desenvolvido com Node.js, Express e TypeScript, disponibilizando endpoints para consulta, cadastro, edição e exclusão de livros.

Os dados são armazenados temporariamente em memória durante a execução da aplicação.

## Tecnologias Utilizadas

### Front-end

* HTML5
* CSS3
* JavaScript
* Fetch API

### Back-end

* Node.js
* Express.js
* TypeScript

## Funcionalidades

* Cadastrar livros
* Listar livros cadastrados
* Editar livros cadastrados
* Excluir livros cadastrados
* Comunicação entre cliente e servidor utilizando Fetch API
* Armazenamento temporário dos dados em memória

## Estrutura do Projeto

BibliotecaOnline

* client

  * index.html
  * style.css
  * script.js

* server

  * src

    * interfaces

      * ILivro.ts

    * data

      * livros.ts

    * server.ts

  * package.json
  * package-lock.json
  * tsconfig.json

## Como Executar o Projeto

### 1. Abrir o Projeto

Abra a pasta **BibliotecaOnline** no Visual Studio Code.

### 2. Instalar as Dependências

Abra um terminal dentro da pasta **server** e execute:

```bash
npm install
```

Esse comando instalará todas as dependências necessárias para o funcionamento do servidor.

### 3. Iniciar o Servidor

Ainda no terminal da pasta **server**, execute:

```bash
npm run dev
```

Se tudo estiver correto, será exibida a mensagem:

```text
Servidor rodando na porta 3000
```

O terminal deve permanecer aberto durante a utilização do sistema.

### 4. Executar o Cliente

Abra o arquivo:

```text
client/index.html
```

em um navegador web de sua preferência.

### 5. Utilização do Sistema

#### Cadastrar Livro

1. Preencha o campo **Título**.
2. Preencha o campo **Autor**.
3. Informe o **Ano de Publicação**.
4. Clique no botão **Cadastrar**.
5. O livro será enviado para o servidor através da API.
6. A lista de livros será atualizada automaticamente na tela.

#### Editar Livro

1. Clique no botão **Editar** ao lado do livro desejado.
2. Os dados do livro serão carregados nos campos do formulário.
3. Altere as informações desejadas.
4. Clique novamente no botão **Cadastrar** para salvar as alterações.

#### Excluir Livro

1. Clique no botão **Excluir** ao lado do livro desejado.
2. O livro será removido imediatamente da lista.

## Endpoints da API

### Listar Livros

**GET /livros**

Retorna todos os livros cadastrados.

---

### Cadastrar Livro

**POST /livros**

Recebe um objeto JSON contendo:

```json
{
  "titulo": "Dom Casmurro",
  "autor": "Machado de Assis",
  "anoPublicacao": 1899
}
```

e adiciona o livro à lista armazenada em memória.

---

### Atualizar Livro

**PUT /livros/:id**

Atualiza os dados de um livro existente.

Exemplo:

```http
PUT /livros/1
```

Recebe um objeto JSON contendo:

```json
{
  "titulo": "Dom Casmurro - Atualizado",
  "autor": "Machado de Assis",
  "anoPublicacao": 1900
}
```

e atualiza as informações do livro correspondente.

---

### Excluir Livro

**DELETE /livros/:id**

Remove um livro da lista utilizando seu identificador.

Exemplo:

```http
DELETE /livros/1
```

O livro correspondente ao identificador informado será removido da lista armazenada em memória.
## Referências Bibliográficas

* ADRIANO, Thiago da Silva. Guia Prático de TypeScript.
* HAVERBEKE, Marijn. Eloquent JavaScript.
* Documentação Oficial do Node.js.
* Documentação Oficial do Express.js.
* MDN Web Docs.
* Material disponibilizado em aula pelo professor.
