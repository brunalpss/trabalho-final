<a href="#"><img src="https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg" width="200"/></a> <a href="#"><img src="https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg" width="250"/></a>

---

# 🔧 OficinaPro 👨‍💻

> [!NOTE]
> **OficinaPro** é um sistema de gestão para oficinas mecânicas automotivas de pequeno e médio porte. Ele centraliza todo o ciclo de atendimento — do agendamento e abertura da Ordem de Serviço (OS) à elaboração de orçamentos, execução, controle de estoque de peças e faturamento — entregando **rastreabilidade**, **histórico por veículo** e **visibilidade do reparo para o cliente**.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O <b>OficinaPro</b> nasceu para substituir os controles manuais (papel e planilhas) que ainda predominam em oficinas, eliminando a perda de histórico de manutenção, a precificação inconsistente de orçamentos e a falta de rastreabilidade no consumo de peças. A aplicação oferece um fluxo padronizado de <i>Ordem de Serviço</i>, <i>orçamento aprovável remotamente pelo cliente</i> e <i>baixa automática de estoque</i>, organizando em um só lugar clientes, veículos, serviços, peças e pagamentos. Este repositório concentra o <b>projeto, a diagramação e a arquitetura</b> da aplicação, documentados com diagramas <b>UML em PlantUML</b>.
      </div>
    </td>
    <td>
      <div>
        <img src="https://joaopauloaramuni.github.io/image/logo_ES_vertical.png" alt="Logo do Projeto" width="120px"/>
      </div>
    </td>
  </tr>
</table>

---

## 🚧 Status do Projeto

![Versão](https://img.shields.io/badge/Versão-v1.0.0-007ec6?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Em%20Projeto-yellow?style=for-the-badge)
![React](https://img.shields.io/badge/React-19.1.1-007ec6?style=for-the-badge&logo=react&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7.1.2-007ec6?style=for-the-badge&logo=vite&logoColor=white)
![Java](https://img.shields.io/badge/Java-17-007ec6?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3.5-007ec6?style=for-the-badge&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-ready-007ec6?style=for-the-badge&logo=docker&logoColor=white)
![Licença](https://img.shields.io/badge/Licença-MIT-007ec6?style=for-the-badge&logo=opensourceinitiative)

---

## 📚 Índice
- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Instalação e Execução](#-instalação-e-execução)
- [Deploy](#-deploy)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Demonstração](#-demonstração)
- [Testes](#-testes)
- [Documentações utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Contribuição](#-contribuição)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

---

## 🔗 Links Úteis
* 🌐 **Demo Online:** [Acesse a Aplicação Web](https://oficinapro.vercel.app)
  > 💻 Aplicação web em ambiente de produção (hospedada na Vercel).
* 📱 **Download Mobile:** [Google Play](https://play.google.com/store) | [APK Direto](https://oficinapro.vercel.app/app-release.apk)
  > 📱 Aplicativo de acompanhamento de OS para o cliente (companion app — opcional).
* 📖 **Documentação:** [Swagger/OpenAPI](https://api.oficinapro.com/swagger-ui.html) | [Documentação de Projeto (UML)](./docs/OficinaPro_Documentacao_de_Projeto.docx)
  > 📚 Documentação técnica da API e documento de projeto com os diagramas UML.

---

## 📝 Sobre o Projeto

O **OficinaPro** é um sistema de gestão de oficinas mecânicas desenvolvido como projeto acadêmico da disciplina **Projeto de Software**.

- **Por que ele existe:** muitas oficinas ainda operam com cadernos e planilhas, o que gera retrabalho, perda de histórico e orçamentos inconsistentes.
- **Qual problema resolve:** centraliza o ciclo de atendimento (agendamento → OS → orçamento → execução → pagamento) e dá rastreabilidade ao consumo de peças e ao status do reparo.
- **Qual o contexto:** acadêmico, com foco em modelagem, diagramação e arquitetura (sem implementação de código), conforme o escopo do trabalho.
- **Onde pode ser utilizado:** oficinas mecânicas automotivas de pequeno e médio porte.

O sistema entrega valor ao **cliente** (transparência sobre o reparo e aprovação remota de orçamento), ao **atendente** (padronização da OS e do orçamento) e ao **gerente** (controle de estoque com alerta de mínimo e relatórios gerenciais).

> [!NOTE]
> Esta seção segue boas práticas de documentação profissional e foi adaptada ao domínio de oficinas mecânicas.

---

## ✨ Funcionalidades Principais

- 🔐 **Autenticação Segura:** Login com perfis (Atendente, Mecânico, Gerente) via JWT.
- 🗓️ **Agendamento de Serviços:** Marcação de horários por cliente e veículo.
- 🧾 **Ordem de Serviço (OS):** Abertura, atribuição de mecânico e acompanhamento de status.
- 💰 **Orçamentos:** Composição com serviços e peças, envio e aprovação/recusa pelo cliente.
- 🛠️ **Controle de Estoque:** Baixa automática de peças, histórico de movimentação e alerta de estoque mínimo.
- 💳 **Faturamento:** Registro de pagamento (dinheiro, cartão, PIX) com integração a gateway externo.
- 📈 **Painel e Relatórios:** Visão gerencial de OS, faturamento e giro de peças.
- 📨 **Notificações:** Avisos por e-mail sobre orçamento pronto e OS concluída.

---

## 🛠 Tecnologias Utilizadas

As seguintes ferramentas e bibliotecas foram (fictíciamente) definidas para o projeto. Recomenda-se o uso das versões listadas (ou superiores).

### 💻 Front-end
* **Framework/Biblioteca:** React v19
* **Linguagem:** TypeScript / JavaScript ES6+
* **Estilização:** Tailwind CSS
* **Gerenciamento de Estado:** Context API + React Query
* **Build Tool:** Vite v7

### 🖥️ Back-end
* **Linguagem/Runtime:** Java 17 (JDK)
* **Framework:** Spring Boot 3.3.x
* **Banco de Dados:** PostgreSQL 16
* **ORM:** Hibernate / Spring Data JPA
* **Autenticação:** Spring Security + JWT

### ⚙️ Infraestrutura & DevOps
* **Containerização:** Docker + Docker Compose
* **Cloud:** AWS (EC2 para a API, RDS para o banco) + Vercel (front-end)
* **CI/CD:** GitHub Actions + SonarQube

---

## 🏗 Arquitetura

A arquitetura segue um modelo **em camadas** com forte separação de responsabilidades, inspirado na **Clean Architecture** e organizado de modo análogo aos níveis do **C4 Model**. A camada de domínio é independente de framework, e o acesso a recursos externos (banco, gateway de pagamento, e-mail) ocorre via **adaptadores**, favorecendo testabilidade e baixo acoplamento.

**Camadas:**
- **Apresentação (SPA React + Vite):** interface consumida pelos usuários.
- **API REST (Controllers + Spring Security):** expõe endpoints, valida entrada e aplica JWT.
- **Aplicação (Services / Casos de Uso):** orquestra regras de negócio e converte entidades em DTOs.
- **Domínio (Entidades + Regras de Negócio):** núcleo do sistema.
- **Infraestrutura:** repositórios Spring Data JPA e adaptadores externos.

**Padrões adotados:** Repository, Service Layer, DTO e Adapter.

### Exemplos de diagramas

> Os diagramas completos (PlantUML) estão no documento de projeto e na pasta `./docs/diagramas`.

| Diagrama de Arquitetura | Diagrama de Classes |
| :---: | :---: |
| <img src="./docs/diagramas/arquitetura.png" alt="Arquitetura em camadas" width="320px"> | <img src="./docs/diagramas/classes.png" alt="Diagrama de Classes" width="200px"> |
| **Modelo de Dados (ER)** | **Casos de Uso** |
| <img src="./docs/diagramas/er_dados.png" alt="Modelo de Dados" width="320px"> | <img src="./docs/diagramas/usecase.png" alt="Casos de Uso" width="200px"> |

---

## 🔧 Instalação e Execução

### Pré-requisitos
* **Java JDK:** Versão **17** ou superior
* **Node.js:** Versão LTS (v18.x ou superior)
* **Gerenciador de Pacotes:** npm ou yarn
* **Docker** (recomendado para o banco de dados)

### 🔑 Variáveis de Ambiente

#### Back-end (Spring Boot)

| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `SERVER_PORT` | Porta do Back-end. | `8080` |
| `SPRING_DATASOURCE_URL` | URL JDBC (PostgreSQL). | `jdbc:postgresql://localhost:5432/oficinapro` |
| `SPRING_DATASOURCE_USERNAME` | Usuário do banco. | `postgres` |
| `SPRING_DATASOURCE_PASSWORD` | Senha do banco. | `senha-segura-123` |
| `JWT_SECRET` | Chave para assinatura de tokens. | `chave_super_segura_base64` |
| `PAYMENT_GATEWAY_KEY` | Chave da API do gateway de pagamento. | `sk_test_...` |

#### Front-end (React, Vite)

Crie um arquivo **`.env.local`** na pasta `/frontend`:

```
VITE_API_URL=http://localhost:8080/api
VITE_PAYMENT_PUBLIC_KEY=pk_test_sua_chave_aqui
```

> **Obs:** variáveis em projetos **Vite** precisam começar com `VITE_` para serem expostas ao bundle do front-end.

### 📦 Instalação de Dependências

```bash
git clone https://github.com/<seu-usuario>/oficinapro.git
cd oficinapro
```

#### Front-end (React)
```bash
cd frontend
npm install
cd ..
```

#### Back-end (Spring Boot)
```bash
cd backend
./mvnw clean install
cd ..
```

### 💾 Inicialização do Banco de Dados (PostgreSQL)

```bash
docker run --name oficinapro_db -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=senha-segura-123 -e POSTGRES_DB=oficinapro -p 5432:5432 -d postgres:16
```

O Spring Boot gerencia o schema no startup (Hibernate `ddl-auto` ou Flyway), então nenhuma migração manual é necessária no ambiente de desenvolvimento.

### ⚡ Como Executar a Aplicação

#### Terminal 1: Back-end
```bash
cd backend
./mvnw spring-boot:run
```
🚀 *Back-end disponível em **http://localhost:8080**.*

#### Terminal 2: Front-end
```bash
cd frontend
npm run dev
```
🎨 *Front-end disponível em **http://localhost:5173**.*

#### 🐳 Execução completa com Docker Compose

```bash
docker-compose up --build -d
```
> [!NOTE]
> `--build` regenera as imagens e `-d` executa em segundo plano. Use `docker ps` para verificar e `docker-compose down` para parar.

---

## 🚀 Deploy

```bash
# 1. Build do Front-end (gera /dist)
cd frontend
npm run build

# 2. Build do Back-end (gera o .jar em /target)
cd ../backend
./mvnw clean package
```

Configure as variáveis de produção no provedor (AWS/Vercel) e execute:

```bash
java -jar backend/target/oficinapro-0.0.1-SNAPSHOT.jar
```

> 🔑 **Variáveis cruciais:** `SPRING_DATASOURCE_URL` (Back-end) e `VITE_API_URL` (Front-end).

---

## 📂 Estrutura de Pastas

```
.
├── .gitignore
├── README.md
├── docker-compose.yml
│
├── /docs                        # 📚 Documentação e diagramas
│   ├── OficinaPro_Documentacao_de_Projeto.docx
│   └── /diagramas               # 🖼️ Diagramas PlantUML (.puml e .png)
│
├── /frontend                    # 📁 Aplicação React
│   ├── /public
│   ├── /src
│   │   ├── /components          # 🧱 Componentes de UI
│   │   ├── /pages               # 📄 Páginas (OS, Orçamento, Estoque, Login)
│   │   ├── /services            # 🔌 Chamadas HTTP à API
│   │   ├── /hooks               # 🎣 Hooks personalizados
│   │   └── /utils               # 🛠️ Utilitários
│   └── package.json
│
├── /backend                     # 📁 Aplicação Spring Boot
│   ├── /src/main/java/com/oficinapro
│   │   ├── /controller          # 🎮 Endpoints REST
│   │   ├── /service             # ⚙️ Casos de uso / regras de negócio
│   │   ├── /repository          # 🗄️ Repositórios JPA
│   │   ├── /model               # 🧬 Entidades (OrdemServico, Orcamento, Peca...)
│   │   ├── /dto                 # ✉️ DTOs
│   │   ├── /config              # 🔧 Configurações (Security, Swagger, CORS)
│   │   ├── /exception           # 💥 Handlers globais
│   │   └── /adapter             # 🔌 Adaptadores (Gateway Pagamento, E-mail)
│   ├── /src/main/resources
│   │   └── application.yml
│   └── pom.xml
│
└── /tests                        # 🧪 Testes E2E
```

---

### 💻 Exemplo de Saída no Terminal (API)

```bash
# Lista as ordens de serviço em aberto
curl -X GET 'http://localhost:8080/api/v1/ordens?status=ABERTA' \
     -H 'Authorization: Bearer <seu-jwt-token>'
```

**Saída Esperada:**
```json
{
  "total": 1,
  "ordens": [
    {
      "numero": 1042,
      "veiculo": { "placa": "ABC1D23", "modelo": "Gol 1.6" },
      "status": "ABERTA",
      "mecanico": "Carlos Souza"
    }
  ]
}
```

---

## 🧪 Testes

### Testes Unitários e de Integração (Back-end)
```bash
cd backend
./mvnw test
```
*Ferramentas: JUnit 5, Mockito.*

### Testes End-to-End (E2E)
```bash
cd frontend
npm run test:e2e
```
*Ferramenta: Cypress.*

---

## 🔗 Documentações utilizadas

* 📖 **Front-end:** [Documentação Oficial do React](https://react.dev/reference/react)
* 📖 **Build Tool:** [Guia de Configuração do Vite](https://vitejs.dev/config/)
* 📖 **Back-end:** [Documentação do Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/html/)
* 📖 **Modelagem:** [PlantUML](https://plantuml.com/)
* 📖 **Containerização:** [Documentação do Docker](https://docs.docker.com/)
* 📖 **Padrão de Commits:** [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

---

## 👥 Autores

| 👤 Nome | :octocat: GitHub | 💼 LinkedIn |
|---------|-----------------|-------------|
| Bruna Lopes  | [@brunalpss](https://github.com/brunalpss) | [Bruna](https://www.linkedin.com/in/bruna-lopes-de-souza/) |

---

## 🤝 Contribuição

1. Faça um `fork` do projeto.
2. Crie uma branch (`git checkout -b feature/minha-feature`).
3. Commit suas mudanças (`git commit -m 'feat: adiciona funcionalidade X'`). **(Utilize [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/))**
4. Faça o `push` (`git push origin feature/minha-feature`).
5. Abra um **Pull Request**.

> [!IMPORTANT]
> Consulte o arquivo [`CONTRIBUTING.md`](./CONTRIBUTING.md) para o guia de estilo e o processo de submissão.

---

## 🙏 Agradecimentos

* [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo apoio institucional e fomento às boas práticas de engenharia.
* [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos ensinamentos sobre **Arquitetura de Software** e **Padrões de Projeto**.

---

## 📄 Licença

Este projeto é distribuído sob a **[Licença MIT](https://opensource.org/licenses/MIT)**.

---
