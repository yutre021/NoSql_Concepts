# NoSql_Concepts
The Concepts of NoSql

# NoSQL vs. Relational Databases: A Comparison (NoSQL vs. Bancos de Dados Relacionais: Uma Comparação)

Databases are fundamental components of almost any software system, storing and managing data. The choice between relational (SQL) and non-relational (NoSQL) databases depends heavily on the specific needs of an application, considering factors like data structure, scalability requirements, and transaction integrity. This document outlines the key characteristics of both paradigms.

---

## English Version

### Relational Databases

Relational databases are based on the relational model, which organizes data into tables, rows, and columns. They are known for their structured approach and strong consistency.

* **Use tables/rows/columns:** Data is stored in a structured format, resembling a spreadsheet, with predefined relationships between tables.
* **Need a predefined schema/complicated to change:** Before data can be added, the structure (schema) of the tables must be explicitly defined. Altering this schema (e.g., adding a new column) can be complex and time-consuming, especially for large datasets.
* **Slow queries when joining multiple tables:** While joins are powerful for relating data, performing complex joins across many large tables can be computationally intensive and lead to slower query performance.
* **Vertically scalable:** Relational databases primarily scale by adding more power to a single server (e.g., more CPU, RAM, faster storage).
    * **Scale by adding more power (e.g., CPU, RAM...)**
    * **More expensive:** Vertical scaling typically involves upgrading hardware, which can become prohibitively expensive as requirements grow.
* **Guarantee ACID transactions:** Relational databases strongly adhere to ACID properties (Atomicity, Consistency, Isolation, Durability), ensuring that transactions are processed reliably, maintaining data integrity even during failures.
* **Typically closed source:** Many traditional relational database systems are proprietary or closed-source, although open-source options exist (e.g., PostgreSQL, MySQL).

### NoSQL Databases

NoSQL (originally "not only SQL") databases provide a flexible and scalable alternative to the relational model. They encompass a variety of data models, including document, key-value, column-family, and graph.

* **Originally non-SQL/non-relational:** These databases emerged as alternatives to traditional SQL databases, offering different ways to store and retrieve data.
* **Not only SQL:** The term "NoSQL" now often means "Not only SQL," indicating that while some may support SQL-like query languages, their fundamental data model is not relational.
* **Non-relational databases:** Their data models vary significantly from the rigid table-based structure of relational databases.
* **Don't use tables/rows/columns:** Instead, they use diverse structures like documents (JSON/BSON), key-value pairs, wide columns, or graphs.
* **Schema-less/easy changes:** Most NoSQL databases are schema-less or offer flexible schemas, meaning data can be added without a predefined structure. This allows for easier and faster changes to the data model as application requirements evolve.
* **Fast queries:** Queries within a single document or simple key-value lookups can be extremely fast due to their optimized data models for specific access patterns and avoidance of complex joins.
* **Horizontal scalable/cheaper:** NoSQL databases are designed for horizontal scalability, meaning they can scale by adding more servers to a distributed cluster rather than upgrading a single powerful server. This is generally more cost-effective.
* **Most don't support ACID transactions:** While some NoSQL databases offer partial ACID compliance, many prioritize availability and partition tolerance over strict consistency (following the CAP theorem), meaning full ACID guarantees are not always provided across distributed operations.
* **Open source:** A significant number of NoSQL databases are open-source projects, which can offer cost advantages and community support.

---

## Versão em Português

# NoSQL vs. Bancos de Dados Relacionais: Uma Comparação

Bancos de dados são componentes fundamentais de quase todo sistema de software, armazenando e gerenciando dados. A escolha entre bancos de dados relacionais (SQL) e não relacionais (NoSQL) depende muito das necessidades específicas de uma aplicação, considerando fatores como estrutura de dados, requisitos de escalabilidade e integridade transacional. Este documento descreve as principais características de ambos os paradigmas.

---

## Versão em Português

### Bancos de Dados Relacionais

Bancos de dados relacionais são baseados no modelo relacional, que organiza os dados em tabelas, linhas e colunas. Eles são conhecidos por sua abordagem estruturada e forte consistência.

* **Usam tabelas/linhas/colunas:** Os dados são armazenados em um formato estruturado, semelhante a uma planilha, com relacionamentos predefinidos entre as tabelas.
* **Precisam de um esquema predefinido/complicado para mudar:** Antes que os dados possam ser adicionados, a estrutura (esquema) das tabelas deve ser explicitamente definida. Alterar esse esquema (ex: adicionar uma nova coluna) pode ser complexo e demorado, especialmente para grandes conjuntos de dados.
* **Consultas lentas ao unir múltiplas tabelas:** Embora as junções sejam poderosas para relacionar dados, a realização de junções complexas em muitas tabelas grandes pode ser computacionalmente intensiva e levar a um desempenho de consulta mais lento.
* **Escaláveis verticalmente:** Bancos de dados relacionais escalam principalmente adicionando mais poder a um único servidor (ex: mais CPU, RAM, armazenamento mais rápido).
    * **Escalam adicionando mais poder (ex: CPU, RAM...)**
    * **Mais caros:** A escalabilidade vertical tipicamente envolve a atualização de hardware, o que pode se tornar proibitivamente caro à medida que os requisitos aumentam.
* **Garantem transações ACID:** Bancos de dados relacionais aderem fortemente às propriedades ACID (Atomicidade, Consistência, Isolamento, Durabilidade), garantindo que as transações sejam processadas de forma confiável, mantendo a integridade dos dados mesmo durante falhas.
* **Tipicamente de código fechado:** Muitos sistemas de banco de dados relacionais tradicionais são proprietários ou de código fechado, embora existam opções de código aberto (ex: PostgreSQL, MySQL).

### Bancos de Dados NoSQL

NoSQL (originalmente "não apenas SQL") fornecem uma alternativa flexível e escalável ao modelo relacional. Eles englobam uma variedade de modelos de dados, incluindo documento, chave-valor, coluna-família e grafo.

* **Originalmente não-SQL/não-relacional:** Esses bancos de dados surgiram como alternativas aos bancos de dados SQL tradicionais, oferecendo diferentes maneiras de armazenar e recuperar dados.
* **Não apenas SQL:** O termo "NoSQL" agora frequentemente significa "Não apenas SQL", indicando que, embora alguns possam suportar linguagens de consulta semelhantes ao SQL, seu modelo de dados fundamental não é relacional.
* **Bancos de dados não relacionais:** Seus modelos de dados variam significativamente da estrutura rígida baseada em tabelas dos bancos de dados relacionais.
* **Não usam tabelas/linhas/colunas:** Em vez disso, usam estruturas diversas como documentos (JSON/BSON), pares chave-valor, colunas largas ou grafos.
* **Sem esquema/mudanças fáceis:** A maioria dos bancos de dados NoSQL não possui esquema ou oferece esquemas flexíveis, o que significa que os dados podem ser adicionados sem uma estrutura predefinida. Isso permite mudanças mais fáceis e rápidas no modelo de dados à medida que os requisitos da aplicação evoluem.
* **Consultas rápidas:** Consultas dentro de um único documento ou buscas simples por chave-valor podem ser extremamente rápidas devido aos seus modelos de dados otimizados para padrões de acesso específicos e à evitação de junções complexas.
* **Escaláveis horizontalmente/mais baratos:** Bancos de dados NoSQL são projetados para escalabilidade horizontal, o que significa que podem escalar adicionando mais servidores a um cluster distribuído em vez de atualizar um único servidor poderoso. Isso é geralmente mais econômico.
* **A maioria não suporta transações ACID:** Embora alguns bancos de dados NoSQL ofereçam conformidade ACID parcial, muitos priorizam a disponibilidade e a tolerância a partição em detrimento da consistência estrita (seguindo o teorema CAP), o que significa que garantias ACID completas nem sempre são fornecidas em operações distribuídas.
* **Código aberto:** Um número significativo de bancos de dados NoSQL são projetos de código aberto, o que pode oferecer vantagens de custo e suporte da comunidade.
