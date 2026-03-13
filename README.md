# 🏦 Banco de Todos

Projeto acadêmico de modelagem e implementação de um **sistema bancário
relacional** utilizando **SQL e MySQL**.

O objetivo do projeto é demonstrar a construção de um banco de dados
completo para operações bancárias, incluindo **contas, clientes,
transações e instituições financeiras**, servindo como base para estudos
de **modelagem de dados, SQL e sistemas financeiros**.

Este repositório pode ser utilizado em disciplinas como:

-   Banco de Dados
-   Programação Backend
-   Engenharia de Software
-   Modelagem de Sistemas

------------------------------------------------------------------------

# 📌 Objetivos do Projeto

Este projeto foi desenvolvido com os seguintes objetivos:

-   Demonstrar **modelagem de banco de dados relacional**
-   Aplicar conceitos de **normalização**
-   Criar **tabelas com chaves primárias**
-   Implementar **chaves estrangeiras**
-   Simular **operações bancárias**
-   Servir como base para **exercícios SQL**

------------------------------------------------------------------------

# 🧱 Estrutura do Banco de Dados

O banco de dados **BANCO_DE_TODOS** foi projetado para representar um
sistema bancário simplificado.

Principais entidades do sistema:

  Tabela            Descrição
  ----------------- ----------------------------------
  BANCOS            Instituições financeiras
  TIPOS_CONTA       Tipos de contas bancárias
  CONTAS            Contas bancárias dos clientes
  TIPOS_TRANSACAO   Categorias de transações
  TRANSACOES        Operações financeiras realizadas

------------------------------------------------------------------------

# 📊 Modelo Conceitual Simplificado

    BANCOS
      │
      └── CONTAS
            │
            └── TRANSACOES
                  │
                  └── TIPOS_TRANSACAO

    TIPOS_CONTA ─── CONTAS

------------------------------------------------------------------------

# 🗄️ Tecnologias Utilizadas

-   SQL
-   MySQL / MariaDB
-   Engine InnoDB
-   Modelagem relacional

------------------------------------------------------------------------

# ⚙️ Como Criar o Banco

Execute o script SQL presente no repositório.

``` sql
CREATE DATABASE BANCO_DE_TODOS;

USE BANCO_DE_TODOS;
```

Depois execute os scripts de criação das tabelas.

------------------------------------------------------------------------

# 🧾 Exemplo de Estrutura de Tabela

``` sql
CREATE TABLE TIPOS_CONTA (
    ID TINYINT UNSIGNED PRIMARY KEY AUTO_INCREMENT,
    CODIGO VARCHAR(20) NOT NULL UNIQUE,
    DESCRICAO VARCHAR(120) NOT NULL
) ENGINE=InnoDB;
```

A utilização da **engine InnoDB** permite:

-   Suporte a **transações**
-   **Integridade referencial**
-   Uso de **foreign keys**
-   Controle de concorrência

------------------------------------------------------------------------

# 🔗 Exemplos de Operações

### Criar uma conta

``` sql
INSERT INTO CONTAS (...)
VALUES (...);
```

### Registrar uma transação

``` sql
INSERT INTO TRANSACOES (...)
VALUES (...);
```

### Consultar saldo de uma conta

``` sql
SELECT SUM(valor)
FROM TRANSACOES
WHERE conta_id = 1;
```

------------------------------------------------------------------------

# 📚 Conceitos Demonstrados

O projeto explora diversos conceitos importantes:

-   Modelagem de banco de dados
-   Integridade referencial
-   Foreign Keys
-   Normalização
-   Estrutura de dados financeiros
-   Operações bancárias

------------------------------------------------------------------------

# 🎓 Aplicação Acadêmica

Este projeto pode ser utilizado para:

-   Exercícios de **SQL**
-   Estudos de **modelagem de dados**
-   Simulação de **sistemas bancários**
-   Práticas em disciplinas de banco de dados

------------------------------------------------------------------------

# 🚀 Possíveis Extensões

Este projeto pode evoluir para incluir:

-   API REST com **Node.js + Express**
-   Integração com **ORM (Prisma / Sequelize)**
-   Interface Web
-   Sistema de autenticação
-   Simulação de **PIX**
-   Sistema de auditoria de transações

------------------------------------------------------------------------

# 👨‍💻 Autor

**Érico Borgonove**

Professor e Desenvolvedor

GitHub:\
https://github.com/EricoBorgonove

------------------------------------------------------------------------

# 📜 Licença

Projeto destinado para **fins educacionais e acadêmicos**.
