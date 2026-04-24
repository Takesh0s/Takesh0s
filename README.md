# 👨🏻‍💻 Luiz Phillipe

**`Desenvolvedor Backend | Java & APIs Seguras`**

Me chamo Luiz Phillipe, tenho 21 anos e sou natural de Brasília. Concluí o ensino médio no CACT (Colégio Adventista de Taguatinga), com o curso técnico em informática, e atualmente curso Engenharia de Software na UCB.

Sou apaixonado por tecnologia, com foco em desenvolvimento backend utilizando Java e construção de APIs seguras e bem estruturadas.

Compartilho meu aprendizado e projetos através do meu canal no YouTube e Instagram, com o objetivo de ajudar outros desenvolvedores a evoluírem na programação.

---

<p align="left">
    <a href="https://www.youtube.com/@takeshi7275">
        <img 
            alt="youtube subscribers" 
            title="Inscreva-se no meu canal" 
            src="https://custom-icon-badges.demolab.com/youtube/channel/subscribers/UCBy4V64XsUKwa74vN-JpEOg?color=%23E05D44&label=Inscreva-se&logo=video&logoColor=white&style=for-the-badge&labelColor=CE4630"
        />
    </a>
    <a href="https://www.youtube.com/@takeshi7275">
        <img 
            alt="youtube views" 
            title="Visualizações no YouTube" 
            src="https://custom-icon-badges.demolab.com/youtube/channel/views/UCBy4V64XsUKwa74vN-JpEOg?color=%23E1AD0E&logo=eye&logoColor=white&style=for-the-badge&labelColor=C79600"
        />
    </a> 
    <a href="https://github.com/Takesh0s?tab=repositories&sort=stargazers">
        <img 
            alt="Total de estrelas" 
            title="Total de estrelas GitHub" 
            src="https://custom-icon-badges.demolab.com/github/stars/Takesh0s?color=55960c&style=for-the-badge&labelColor=488207&logo=star&label=estrelas"
        />
    </a>
    <a href="https://github.com/Takesh0s?tab=followers">
        <img 
            alt="Seguidores" 
            title="Me siga no GitHub" 
            src="https://custom-icon-badges.demolab.com/github/followers/Takesh0s?color=236ad3&labelColor=1155ba&style=for-the-badge&logo=github&label=Seguidores&logoColor=white"
        />
    </a>
    <a href="https://www.linkedin.com/in/luiz-phillipe-499078203/">
        <img 
            alt="LinkedIn" 
            title="Me conecte no LinkedIn" 
            src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"
        />
    </a>
</p>

---

## 🧠 Habilidades

* Desenvolvimento de APIs REST com Spring Boot
* Autenticação e autorização (JWT, Spring Security, BCrypt)
* Modelagem de banco de dados relacional (PostgreSQL, MySQL)
* Arquitetura em camadas (Controller, Service, Repository)
* Tratamento global de exceções
* Organização de código com DTOs e boas práticas
* Frontend com React + TypeScript e integração mobile via Capacitor
* BaaS com Supabase (PostgreSQL + Auth + PostgREST)

---

## 🚀 Projetos

### 🎲 RollCore — Plataforma de RPG de Mesa

📌 Plataforma completa (Web + Mobile + API) para rolagem de dados e gerenciamento de personagens de RPG de mesa, com foco em conformidade com casos de uso, arquitetura modular e experiência visual imersiva.

🔗 https://github.com/Takesh0s/RollCore · 🌐 https://rollcore.vercel.app/

**Stack:** React 18 + TypeScript · Vite · Zustand · Capacitor (iOS/Android) · Spring Boot 3 · PostgreSQL 16 · JWT · Flyway · Docker

**Funcionalidades:**

* Autenticação com JWT e política de senha forte (OWASP)
* Gerenciamento completo de fichas de personagens D&D 5e — atributos, modificadores, HP, slots de magia
* Rolagem de dados com fórmulas `NdX+M`, animações, Acerto/Falha Crítica e histórico das últimas 50 rolagens
* Backend REST com rate limiting (Bucket4j, 60 req/min), Swagger UI e cobertura de testes ≥ 80% (JaCoCo)
* Monorepo com frontend web, app Android/iOS via Capacitor e API Spring Boot

**Arquitetura:**

```
Frontend (React + Vite)  →  REST API (Spring Boot 3)  →  PostgreSQL 16
      ↕ Capacitor               ↕ JWT + BCrypt               ↕ Flyway
  iOS / Android          Spring Security + Bucket4j        Redis (Fase 2)
```

---

### 🧭 Sistema Bússola — Plataforma para Clubes de Desbravadores

📌 Sistema web completo de administração e controle para clubes de desbravadores da Divisão Sul-Americana, com multitenancy real — cada clube opera em isolamento total de dados. Cobre gestão de membros, especialidades com checklist de requisitos, controle financeiro e geração de relatórios em PDF, atendendo todos os requisitos da Especialidade de Informática Programável (AP-052).

🔗 https://github.com/Takesh0s/Sistema-Bussola

**Stack:** HTML5 · CSS3 · JavaScript ES2022 · Supabase (PostgreSQL + Auth + PostgREST + Storage + RLS) · jsPDF

**Arquitetura e segurança:**

* Multitenancy por clube via Row Level Security (RLS) no Supabase — isolamento garantido em nível de banco
* Hierarquia geográfica: União → Associação → Clube
* Sistema de papéis (diretor, diretor associado, secretário, tesoureiro) com convites por token de 7 dias
* Função `security definer` para resolver RLS recursivo em `perfil_usuario`
* Migrations versionadas em ordem cronológica no repositório (`/migrations`)

**Módulos:**

* **Direção** — cadastro de membros com cargo (respeitando gênero), classes concluídas e em andamento; acesso a classes Líder+ restrito a esta aba
* **Desbravadores** — ficha com classe, especialidades em andamento/concluídas e perfil individual
* **Especialidades** — catálogo completo com imagem, requisitos em checklist interativo e hiperlinks entre especialidades dependentes; Mestrados com hiperlinks para as especialidades que os compõem
* **Unidades** — gestão de unidades com conselheiro e associados vinculados
* **Mensalidades** — controle de pagamentos com toggle de status por membro
* **Caixa** — entradas/saídas com saldo em tempo real
* **Patrimônio** — inventário de bens por unidade
* **Atas e Atos** — registros oficiais com visualização e edição
* **Relatórios** — 6 tipos de PDF gerados no cliente via jsPDF (autorização de saída, fluxo de caixa, patrimônio, livro de atas, mensalidades e relatório geral)

**Autenticação:** Login com e-mail/senha e Google OAuth via Supabase Auth, com proteção de rotas e logout seguro.

---

## 🌎 Projeto Complementar

### 🗺️ DF-Turismos

📌 Sistema para divulgação de pontos turísticos do Distrito Federal.

🔗 https://github.com/Takesh0s/DF-Turismos

**Destaques:**

* Evolução em múltiplas versões
* Foco em organização e documentação
* Aplicação prática de conceitos de desenvolvimento

---

## 🤖 Linguagens e Tecnologias

<img 
 align="left"
 alt="Java" 
 title="Java" 
 width="40"
 style="padding-right: 10px;" 
 src="https://github.com/devicons/devicon/blob/master/icons/java/java-original.svg"
/> <img 
 align="left" 
 alt="Spring Boot" 
 title="Spring Boot"
 width="40"
 style="padding-right: 10px;"
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/spring/spring-original.svg"
/> <img 
 align="left" 
 alt="PostgreSQL" 
 title="PostgreSQL"
 width="40"
 style="padding-right: 10px;"
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg"
/> <img 
 align="left" 
 alt="MySQL" 
 title="MySQL"
 width="40"
 style="padding-right: 10px;"
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg"
/> <img 
 align="left" 
 alt="React" 
 title="React"
 width="40"
 style="padding-right: 10px;"
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg"
/> <img 
 align="left" 
 alt="TypeScript"
 title="TypeScript" 
 width="30px" 
 style="padding-right: 10px;" 
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg" 
/> <img 
 align="left" 
 alt="JavaScript" 
 title="JavaScript"
 width="30px" 
 style="padding-right: 10px;" 
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg" 
/> <img 
 align="left" 
 alt="Docker" 
 title="Docker"
 width="40"
 style="padding-right: 10px;"
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/docker/docker-original.svg"
/> <img 
 align="left" 
 alt="Git" 
 title="Git"
 width="30px" 
 style="padding-right: 10px;" 
 src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg" 
/>

<br/>
<br/>

---

## 🎯 Objetivo

Busco oportunidades como desenvolvedor backend para aplicar meus conhecimentos na construção de sistemas reais, evoluir tecnicamente e gerar impacto através da tecnologia.