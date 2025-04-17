
# Cadastro de Pessoas

Este projeto é um sistema simples de cadastro de pessoas com múltiplos endereços, desenvolvido como desafio técnico. Ele utiliza Java EE com foco em boas práticas de arquitetura, experiência do usuário e simplicidade de execução.

---

## 🔧 Tecnologias Utilizadas

- Java EE (Jakarta EE)
- JSF 2.3 com PrimeFaces
- Bootstrap 5 (UX responsiva)
- JPA (Hibernate) para persistência
- EJB para injeção de dependência
- PostgreSQL como banco de dados
- JUnit + H2 para testes
- Maven para build
- Docker (opcional)

---

## 📐 Decisões Técnicas

- Arquitetura MVC: separação entre modelo, controle e visualização.
- PrimeFaces: componentes ricos de interface.
- Bootstrap: layout moderno e responsivo.
- EJB Stateless para regras de negócio.
- JPA com Hibernate para mapeamento objeto-relacional.

---

## ▶️ Como Executar o Projeto

### 1. Pré-requisitos

- JDK 11+
- Maven 3.6+
- Servidor Java EE (WildFly, Payara, GlassFish)
- PostgreSQL (ou Docker)

### 2. Banco de Dados via Docker (Recomendado)

```bash
docker-compose up -d
```

O PostgreSQL estará acessível em `localhost:5432`, com:
- Banco: `cadastrodb`
- Usuário: `postgres`
- Senha: `postgres`

### 3. Configurar o DataSource no Servidor

No servidor de aplicação, crie um datasource com:
- JNDI: `java:/PostgresDS`
- JDBC URL: `jdbc:postgresql://localhost:5432/cadastrodb`
- Usuário: `postgres`
- Senha: `postgres`

### 4. Compilar e Empacotar

```bash
mvn clean package
```

Isso gerará um arquivo `.war` em `target/`. Importe no servidor de aplicação.

### 5. Acessar Aplicação

Acesse `http://localhost:8080/cadastro-pessoas` no navegador.

---

## 🧪 Rodar Testes

Os testes são feitos com H2 (banco em memória):

```bash
mvn test
```

---

## 📌 Notas Finais

- O sistema permite o cadastro de pessoas e múltiplos endereços.
- A experiência do usuário foi aprimorada com Bootstrap e PrimeFaces.
- O projeto é leve, bem organizado e fácil de expandir.
- Código dividido em camadas: modelo, DAO, serviço, controle e visualização.

---

Feito com 💻 e dedicação!
