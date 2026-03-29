 Community Library - API Node.js

Uma API REST robusta desenvolvida com **Node.js**, **Express** e **SQLite**, para gerenciar uma biblioteca comunitária com funcionalidades completas de CRUD para livros, usuários e empréstimos.

![Node.js](https://img.shields.io/badge/Node.js-20.0-339933?style=flat-square&logo=node.js)
![Express](https://img.shields.io/badge/Express-4.0-000000?style=flat-square&logo=express)
![SQLite](https://img.shields.io/badge/SQLite-3.0-003B57?style=flat-square&logo=sqlite)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

   Sobre o Projeto

Community Library é uma API REST completa para gerenciamento de uma biblioteca comunitária. Oferece:

- Gerenciamento de Livros - CRUD completo com busca e filtros
- Gerenciamento de Usuários - Registro, autenticação e perfis
- Sistema de Empréstimos - Controle de empréstimos e devoluções
- Histórico de Transações - Rastreamento completo de movimentações
- Validação de Dados - Validação robusta em todas as operações
- Tratamento de Erros - Respostas de erro padronizadas
- Documentação API - Endpoints bem documentados
- Testes Automatizados - Testes unitários e de integração

    Tecnologias Utilizadas

    Backend
- Node.js 20 - Runtime JavaScript
- Express 4 - Framework web minimalista
- SQLite 3 - Banco de dados leve e portável
- Sequelize - ORM para Node.js
- Joi - Validação de schemas
- JWT - Autenticação com tokens

   Ferramentas
- Git/GitHub - Versionamento de código
- npm - Gerenciador de pacotes
- Jest - Framework de testes
- Postman - Testes de API
- ESLint - Linting de código

    Instalação

   Pré-requisitos
- Node.js 18+ instalado
- npm ou yarn
- Git

   Passos

1. Clone o repositório
   ```bash
   git clone https://github.com/FHPBeto/community_library.git
   cd community_library
   ```

2. Instale as dependências
   ```bash
   npm install
   ```

3. Configure as variáveis de ambiente
   ```bash
   cp .env.example .env
   ```

4. Inicie o servidor
   ```bash
   npm start
   ```

5. Acesse a API
   ```
   http://localhost:3000
   ```

   Estrutura do Projeto

```
community_library/
├── src/
│   ├── controllers/        # Controladores da API
│   ├── models/            # Modelos de dados
│   ├── routes/            # Rotas da API
│   ├── middleware/        # Middlewares
│   ├── validators/        # Validadores
│   ├── utils/             # Utilitários
│   ├── config/            # Configurações
│   ├── database/          # Inicialização do banco
│   └── app.js             # Aplicação principal
├── tests/                 # Testes automatizados
├── package.json           # Dependências
└── server.js              # Ponto de entrada
```

   Endpoints Principais

   Livros
- `GET /api/books` - Listar todos os livros
- `GET /api/books/:id` - Obter livro por ID
- `POST /api/books` - Criar novo livro
- `PUT /api/books/:id` - Atualizar livro
- `DELETE /api/books/:id` - Deletar livro

   Usuários
- `GET /api/users` - Listar usuários
- `POST /api/users/register` - Registrar novo usuário
- `POST /api/users/login` - Login de usuário
- `GET /api/users/:id` - Obter perfil do usuário

   Empréstimos
- `GET /api/loans` - Listar empréstimos
- `POST /api/loans` - Criar novo empréstimo
- `PUT /api/loans/:id/return` - Devolver livro
- `GET /api/loans/user/:userId` - Empréstimos do usuário

   Scripts Disponíveis

```bash
# Inicia servidor em desenvolvimento
npm start

# Inicia com nodemon (reload automático)
npm run dev

# Executa testes
npm test

# Executa testes com cobertura
npm run test:coverage

# Lint do código
npm run lint

# Formata código
npm run format
```

 Autenticação

A API usa **JWT (JSON Web Tokens)** para autenticação:

1. **Registre um usuário** - `POST /api/users/register`
2. **Faça login** - `POST /api/users/login`
3. **Receba um token** - Salve o token retornado
4. **Use o token** - Adicione ao header: `Authorization: Bearer <token>`

   Exemplos de Requisições

   Criar um Livro
```bash
curl -X POST http://localhost:3000/api/books \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <token>" \
  -d '{
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "isbn": "978-0132350884",
    "year": 2008,
    "quantity": 5
  }'
```

   Listar Livros
```bash
curl -X GET http://localhost:3000/api/books \
  -H "Authorization: Bearer <token>"
```

  Testes

   Executar Todos os Testes
```bash
npm test
```

   Executar Testes com Cobertura
```bash
npm run test:coverage
```

   Estatísticas do Projeto

- Endpoints: 15+
- Modelos: 4 (Books, Users, Loans, Transactions)
- Testes: 50+
- Cobertura: 85%+
- Linhas de Código: 3000+

   Próximas Melhorias

- [ ] Implementar paginação avançada
- [ ] Adicionar filtros de busca complexos
- [ ] Implementar notificações por email
- [ ] Adicionar sistema de multas
- [ ] Implementar reservas de livros
- [ ] Adicionar relatórios e estatísticas
- [ ] Implementar rate limiting
- [ ] Adicionar cache com Redis
- [ ] Documentação com Swagger
- [ ] Deploy em produção

    Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para:
- Reportar bugs
- Sugerir melhorias
- Enviar pull requests
- Melhorar documentação

    Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

  Autor

   Humberto - Engenheiro de Software

-  Email: [humberto.software@gmail.com](mailto:humberto.software@gmail.com)
-  LinkedIn: [linkedin.com/in/humberto-jose-oliveira-software](https://linkedin.com/in/humberto-jose-oliveira-software)
-  GitHub: [@FHPBeto](https://github.com/FHPBeto)
-  Portfólio: [humberfolio-ghk7qz9n.manus.space](https://humberfolio-ghk7qz9n.manus.space)

   Contato

Tem dúvidas ou sugestões? Entre em contato através do email ou LinkedIn!

---

"Desenvolvido usando Node.js + Express + SQLite"
