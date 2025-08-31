 # API Node com Fastify e Drizzle ORM
 
 Esta é uma API robusta construída com Node.js, utilizando o framework Fastify para alta performance e o Drizzle ORM para uma interação moderna com o banco de dados PostgreSQL. O projeto inclui autenticação baseada em JWT, hashing de senhas com Argon2 e validação de schemas com Zod.
 
 ## ✨ Funcionalidades
 
 - **Framework Rápido**: Construído sobre o [Fastify](https://www.fastify.io/), um dos frameworks web mais rápidos para Node.js.
 - **ORM Moderno**: Utiliza [Drizzle ORM](https://orm.drizzle.team/) para uma interação type-safe com o banco de dados.
 - **Autenticação Segura**: Implementa autenticação via JWT (JSON Web Tokens).
 - **Hashing de Senhas**: Usa [Argon2](https://en.wikipedia.org/wiki/Argon2) para armazenar senhas de forma segura.
 - **Validação de Dados**: Garante a integridade dos dados com [Zod](https://zod.dev/).
 - **Testes Automatizados**: Configurado com [Vitest](https://vitest.dev/) para testes unitários e de integração.
 - **Documentação de API**: Gera documentação interativa com [Swagger](https://swagger.io/).
 - **TypeScript**: Totalmente escrito em TypeScript para maior segurança e manutenibilidade do código.
 
 ## 🚀 Começando
 
 Siga os passos abaixo para configurar e rodar o projeto em seu ambiente local.
 
 ### Pré-requisitos
 
 - [Node.js](https://nodejs.org/) (versão 20 ou superior)
 - [Docker](https://www.docker.com/) e [Docker Compose](https://docs.docker.com/compose/) (para o banco de dados PostgreSQL)
 
 ### Instalação
 
 1. **Clone o repositório:**
    ```bash
    git clone <url-do-seu-repositorio>
    cd api-node
    ```
 
 2. **Instale as dependências:**
    ```bash
    npm install
    ```
 
 3. **Configure as variáveis de ambiente:**
    Crie um arquivo `.env` na raiz do projeto, você pode usar o `.env.example` como base:
    ```env
    # .env.example
    
    # Ambiente (development, production, test)
    NODE_ENV=development
    
    # URL de conexão com o banco de dados
    DATABASE_URL="postgresql://docker:docker@localhost:5432/api_db"
    
    # Segredo para gerar os tokens JWT
    JWT_SECRET="seu-segredo-aqui"
    ```
 
 4. **Inicie o banco de dados com Docker:**
    Use o comando abaixo para iniciar um contêiner PostgreSQL.
    ```bash
    docker-compose up -d
    ```
 
 5. **Execute as migrações do banco de dados:**
    Este comando irá criar as tabelas necessárias no seu banco de dados.
    ```bash
    npm run db:migrate
    ```
 
 ## 📜 Scripts Disponíveis
 
 - `npm run dev`: Inicia o servidor em modo de desenvolvimento com watch mode.
 - `npm run db:seed`: Popula o banco de dados com dados iniciais (se configurado).
 - `npm run db:generate`: Gera novos arquivos de migração com base nas alterações dos schemas do Drizzle.
 - `npm run db:migrate`: Aplica as migrações pendentes no banco de dados.
 - `npm run db:studio`: Abre o Drizzle Studio, uma interface para visualizar e gerenciar seu banco de dados.
 - `npm run test`: Executa os testes automatizados com Vitest.
 
 ## 📚 Documentação da API
 
 Após iniciar o servidor (`npm run dev`), a documentação interativa da API, gerada pelo Swagger, estará disponível em:
 
 http://localhost:3333/docs
 
 ## 🛠️ Tecnologias Utilizadas
 
 - **Backend**: Fastify, Node.js
 - **Banco de Dados**: PostgreSQL, Drizzle ORM
 - **Testes**: Vitest, Supertest
 - **Validação**: Zod
 - **Autenticação**: JWT, Argon2
 - **Linguagem**: TypeScript