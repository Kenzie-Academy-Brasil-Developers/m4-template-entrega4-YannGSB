# API de Livros

## Descrição do Projeto

Desenvolvi uma API para gerenciamento de uma coleção de livros. A metodologia de Test Driven Development (TDD) foi utilizada, garantindo a qualidade e robustez do código.

### Funcionalidades Principais

1. **Passos Iniciais:**
   - Criação do arquivo `database.ts` para a definição da constante `booksDatabase` e exportação da mesma.

2. **Rotas e Banco de Dados:**
   - Implementação de um roteador (Router) para encapsular as rotas de livros.
   - Criação das rotas de CRUD (POST, GET, GET/:id, PATCH/:id, DELETE/:id) com prefixo /books.
   - Garantia de ids sequenciais e únicos para cada livro adicionado ao banco de dados.

3. **Requisições e Respostas:**
   - Desenvolvimento de requisições e respostas seguindo a arquitetura de controllers e services.
   - Definição de modelos de requisição e padrões de resposta para cada tipo de operação (CREATE, READ, UPDATE, DELETE).

4. **Middlewares:**
   - Implementação de um middleware global de erros para gerenciar todas as exceções da aplicação.
   - Criação de um middleware para verificar a existência do livro por meio do id.
   - Introdução de um middleware para impedir a criação de livros com o mesmo nome.

5. **Atualização com Helmet:**
   - Instalação e configuração do Helmet para fortalecer a segurança da aplicação.

6. **Validação de Dados com Zod:**
   - Adição do Zod como dependência de produção.
   - Criação de um middleware de validação de dados capaz de validar req.params, req.body e req.query.
   - Especificação de esquemas de validação para as rotas POST /books e PATCH /books/:id.

7. **Busca pelo Nome:**
   - Aperfeiçoamento da rota GET /books para permitir busca pelo nome do livro, introduzindo um novo parâmetro opcional.
