# **Definições do projeto**

##### **Haul Manager**

Aplicação web para gerenciamento de pedidos de importações.

## **Estrutura do Projeto**

### **1. Planejamento Inicial**

#### **Escopo**

Aplicação web para gerenciamento de pedido de compras. A aplicação será desenvolvida com foco apenas para usuários desktop. A ideia é que seja um painel para para que importadores gerenciem suas importações. Esse é um projeto, que por sua essência, é para ser simples e não tem objetivo de se tornar algo complexo e com muitas funcionalidades.

#### **Frentes**

Backend e Frontend

---

### **2. Arquitetura do Sistema**

#### **Separação das Frentes**

- Repositório único, com pastas separadas para cada frente do projeto.

#### **Design Patterns**

##### **Frontend**

- **Component-Based Architecture**: componentes reutilizáveis
- **Flux/Redux**: gerenciamento de estado
- **Atomic Design**: criar um design system consistente e reutilizável
- **Container-Presentational Pattern**: separar a lógica de negócios (containers) da lógica de apresentação (presenters).
- **Padrão de Componentes de Layout**: ajuda os desenvolvedores a organizar a estrutura e o layout de suas aplicações

##### **Backend**

- **Repository Pattern**: para abstração das operações do banco de dados.
- **Service Layer**: para encapsular lógica de negócios.
- **MVC (Model-View-Controller)**: separação de responsabilidades entre os componentes do sistema.

#### **Estrutura de Projeto**

Quero o projeto o mais organizado possível, a estrutura deve ser algo fácil de entender e fácil de incluir pequenas novas funcionalidades.

—

### **3. Padrões de Código**

#### **Linters e Formatters**

- ESLint e Prettier para cada frente

#### **Normas de Nomeação**

##### **Variáveis**

- Use `camelCase`
- Nomes descritivos e significativos (e.g., `userBalance` em vez de `ub`)
- Usar `UPPER_SNAKE_CASE` para constantes (e.g., `const MAX_RETRIES`)

##### **Funções**

- Use verbos para funções (e.g., `calculateTotal`, `fetchUserData`).
- Usar camelCase para funções (`function getUserName()`).

##### **Classes**

- Use PascalCase para classes e componentes (e.g., `UserProfile`, `TransactionService`).
- Nomes de classes devem ser substantivos.

#### Versionamento Semântico (SemVer)

**Major.Minor.Patch (1.0.0):**

- **Major**: Mudanças incompatíveis na API.
- **Minor**: Funcionalidades adicionadas de forma compatível.
- **Patch**: Correções de bugs compatíveis.

#### Padrão de Commits

Git + Github + [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

### 4. Documentação

#### Código

**Comentários TSDoc**: Facilita a geração de documentação automática e entendimento do código.
**Swagger/OpenAPI**: Padrões para documentar APIs RESTful, facilitando a integração e uso.

---

### 5. Frontend

#### Linguagens e Frameworks

- **Linguagem**: Typescript (NodeJS)
- **Frameworks/Bibliotecas**: NextJS + [ChakraUI](https://v2.chakra-ui.com/) + Emotion

---

### 6. Backend

#### Linguagens e Frameworks

- **Linguagem**: TypeScript (NodeJS)
- **Frameworks**: Express.js

#### Autenticação e Autorização

- [NextAuth](https://next-auth.js.org/)
- Autenticação de usuários via Google Auth com NextAuth.

#### Segurança

- Validações de entrada.
- Proteção contra XSS, CSRF.
- Encriptação de dados.

---

### 7. Banco de Dados

#### Tipo

- Non-relational: [MongoDB](https://www.mongodb.com/products/platform/atlas-database)

#### ORM/ODM

- [Mongoose ODM](https://www.npmjs.com/package/mongoose)

---

### 8. CI/CD (Continuous Integration / Continuous Deployment) e Infraestrutura

- [Github Actions](https://docs.github.com/pt/actions), [Travis CI](https://www.travis-ci.com/) ou [Cloud Build](https://cloud.google.com/build?hl=pt_br) (caso os serviços fiquem hospedados no GCP) para construção das pipelines
- [Digital Ocean](https://www.digitalocean.com/), [Heroku](https://www.heroku.com/) ou [Cloud Run](https://cloud.google.com/run?hl=pt_br) para implantação da aplicação em produção e staging.
- Vou precisar que o projeto tenha 3 ambientes. Um de desenvolvimento local, um de staging (pré-produção) e por último, um de produção
- Vou precisar que o código seja pensado para ser executado nesses três ambientes (utilização de variável de ambiente para mudar comportamente do código de acordo com o ambiente)

#### Pipelines

1. Build
2. Testes Automatizados (Unitários / Integração)
3. Deploy (para QA e Produção)

---

### 9. Notas extras importantes

- Motivação do projeto: Estou fazendo esse projeto a fim de satisfazer uma necessidade minha, na qual quero aprender, e ao mesmo tempo gerenciar minhas importações. Além disso, vou utilizar essa aplicação como um portfólio.
