# Projeto de Diagramas - Atividades e Fases

Este repositório contém os diagramas e roteiros desenvolvidos durante as diferentes fases do projeto, organizados para facilitar o entendimento e a documentação dos modelos UML e outros artefatos.

- <a href='https://github.com/RafaBricia/diagramas-UML'>Link do repositório</a>
- <a href='https://docs.google.com/document/d/1JjykTTRIHDeu-AFM_2steHJHJFrl7uu31GH0aa0d0Q4/edit?tab=t.0#heading=h.6rhzl4httx7r'>Link do documento fase 1</a>
- <a href='https://docs.google.com/document/d/1s2B4P-pfVWnZSKARpnz-BWcJoRzsWY7IblXpK9uIsAE/edit?tab=t.0#heading=h.6rhzl4httx7r'>Link do documento fase 2</a>

---

## Estrutura do Repositório

### ATIVIDADES
Pasta principal contendo as atividades relacionadas ao projeto.

### FASE1
Contém os diagramas e roteiros referentes à primeira fase do projeto.

- <a href='https://docs.google.com/document/d/1YtV6MRLIJhfSWkv6cyQxK5KoDz20O7vMZstDvg6GJ6w/edit?tab=t.0#heading=h.ug202kq7d4tt'>Link do documento</a>


- **Diagrama_Atividades**  
  Roteiro e documentação do Diagrama de Atividades.  
  Arquivo principal: `roteiroAtividades.md`

- **Diagrama_Componentes**  
  Roteiro e documentação do Diagrama de Componentes.  
  Arquivo principal: `roteiroComponentes.md`

- **Diagrama_Maquina_Estados**  
  Roteiro e documentação do Diagrama de Máquina de Estados.  
  Arquivo principal: `roteiroMaquina_Estados.md`

- **Diagrama_pacotes**  
  Contém o Diagrama de Pacotes em imagem e o roteiro explicativo.  
  Arquivos principais:  
  - `Diagrama_de_pacote.png` (imagem do diagrama)  
  - `roteiroPacote.md`

- **README.md**  
  Arquivo de documentação específico desta fase.

### FASE2
Pasta reservada para os arquivos e atividades da segunda fase do projeto (a ser preenchida).

- <a href='https://docs.google.com/document/d/180VsQ5tG0vIehr7Q8gPnbiZI34hLHC0Aoqu5X1-8qb4/edit?tab=t.0#heading=h.ug202kq7d4tt'>Link do documento</a>


---

## Objetivo

Este repositório tem como objetivo centralizar a documentação dos diagramas UML e seus roteiros para facilitar o desenvolvimento, revisão e apresentação dos modelos do sistema em estudo.

---

## Como usar

- Navegue pelas pastas correspondentes às fases e tipos de diagramas para encontrar as descrições e diagramas específicos.
- Utilize os roteiros (`*.md`) para entender a lógica e as regras aplicadas em cada diagrama.
- Consulte o arquivo `README.md` de cada fase para informações específicas adicionais.

---

## Contato

Para dúvidas ou sugestões, entre em contato com o responsável pelo projeto.

---

*Última atualização: 2025*

###
---

# Projeto Backend - Sistema de Restaurantes e Avaliações

Este projeto consiste em um backend para gerenciamento de restaurantes, pratos, usuários e avaliações. A arquitetura segue boas práticas, com separação clara entre camadas de controllers, repositórios, casos de uso, middlewares e schemas, além de testes automatizados para garantir a qualidade.

---

---

## Tecnologias e Ferramentas

- **Node.js** e **JavaScript**
- **Prisma ORM** para gerenciamento do banco de dados
- Testes automatizados com **Jest**
- Estrutura modular para facilitar manutenção e escalabilidade
- Autenticação e autorização via tokens JWT
- Upload de imagens para restaurantes e pratos

---

## Descrição das Principais Pastas

### Prisma

Contém o arquivo de schema do banco de dados (`schema.prisma`) e migrações para versionamento das alterações no banco.

### Adapters

Funções para geração de IDs, hash de senhas, comparação de senhas e geração/verificação de tokens JWT.

### Controllers

Responsáveis por receber as requisições HTTP, chamar os casos de uso correspondentes e retornar respostas ao cliente. Cada domínio (prato, restaurante, avaliação, usuário) possui seus próprios controllers e testes.

### Errors

Implementações de classes de erro específicas para cada domínio, melhorando o tratamento de exceções e mensagens claras para o cliente.

### Factories

Fábricas para criação dos controllers, facilitando a injeção de dependências e o desacoplamento.

### Middlewares

Middlewares para autenticação JWT, tratamento de upload de imagens e outros processos intermediários nas requisições.

### Repositories

Acesso direto ao banco de dados via Prisma, implementando operações CRUD para cada entidade.

### Routes

Definição das rotas da API, agrupadas por recurso (dishes, restaurants, reviews, users).

### Schemas

Validações dos dados recebidos e enviados pela API para garantir integridade e segurança.

### Tests

Testes unitários e de integração para controllers, use-cases e outras partes do sistema, garantindo robustez e prevenindo regressões.

### Use-Cases

Implementação da lógica de negócio central do sistema, manipulando dados através dos repositórios e aplicando regras específicas.

---

## Como Rodar o Projeto

1. **Instale as dependências:**

```bash
npm install

Configure o banco de dados no arquivo .env (não incluído aqui, mas necessário).

Execute as migrações do Prisma:

```

```bash

npx prisma migrate deploy
Inicie a aplicação:


```

```bash

npm start
Execute os testes:

```

```bash
npm test

```
