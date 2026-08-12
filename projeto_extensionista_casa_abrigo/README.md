# 🏠 Casa do Povo da Rua — Sistema de Controle de Atendimentos

Projeto extensionista desenvolvido durante a graduação em **Ciência da Computação**, com o objetivo de criar uma aplicação desktop para auxiliar no registro e acompanhamento das pessoas atendidas pela **Casa do Povo da Rua**, em Fortaleza/CE.

A proposta surgiu a partir da necessidade de melhorar o controle dos atendimentos realizados pela instituição e facilitar a geração de informações sobre o público atendido.

---

## 🎯 Objetivo

Desenvolver uma ferramenta simples e intuitiva para registrar e acompanhar o fluxo de pessoas atendidas pela Casa do Povo da Rua.

O sistema foi pensado para permitir o registro de informações dos atendimentos e, posteriormente, utilizar esses dados para compreender melhor aspectos como:

- quantidade de pessoas atendidas;
- frequência de retorno à instituição;
- participação nas atividades oferecidas;
- perfil das pessoas atendidas;
- evolução dos atendimentos ao longo do tempo.

A disponibilidade dessas informações também poderia auxiliar a instituição na elaboração de relatórios e na apresentação de dados mais concretos sobre sua atuação.

---

## 💡 Problema

A Casa do Povo da Rua desenvolve ações de acolhimento, recuperação e ressocialização de pessoas em situação de rua.

Durante o levantamento de requisitos, foi identificada a necessidade de possuir um controle mais estruturado sobre as pessoas que frequentavam a instituição.

Sem uma ferramenta adequada, informações importantes sobre atendimentos e frequência poderiam ser difíceis de organizar, consultar e transformar em indicadores.

A proposta do projeto foi, portanto, aplicar conhecimentos de **Programação Orientada a Objetos e Banco de Dados** na construção de uma solução capaz de apoiar esse processo.

---

## 🖥️ Solução Desenvolvida

Foi desenvolvida uma aplicação desktop utilizando **Java e Swing**, estruturada segundo conceitos de Programação Orientada a Objetos.

O sistema foi projetado com três componentes principais:

### 🔐 Autenticação

Tela inicial responsável por solicitar usuário e senha antes de permitir acesso às demais funcionalidades da aplicação.

### 📝 Cadastro

Interface para registro das pessoas atendidas pela instituição, utilizando informações como:

- local;
- data;
- nome;
- sexo;
- ocupação;
- tempo em situação de rua.

Após o cadastro, as informações poderiam ser armazenadas e consultadas posteriormente.

### 📊 Relatórios

Área destinada à consulta dos registros realizados e à geração de informações sobre os atendimentos.

A solução também foi projetada para permitir a exportação dos dados em formatos como:

- CSV;
- Excel (`.xlsx`).

---

## 🏗️ Arquitetura

O projeto utilizou uma arquitetura simples, adequada ao contexto acadêmico e aos requisitos levantados.

```text id="ewj3lp"
┌──────────────────────────┐
│       Interface          │
│       Java Swing         │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│       Aplicação          │
│          Java            │
│            +             │
│ Programação Orientada    │
│      a Objetos           │
└────────────┬─────────────┘
             │
             ▼
┌──────────────────────────┐
│    Persistência local    │
│       SQLite / CSV       │
└──────────────────────────┘
```

A aplicação foi projetada para funcionar localmente, sem necessidade de infraestrutura externa.

---

## 🛠️ Tecnologias Utilizadas

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

Além delas, foram utilizados:

- **Java Swing** — construção da interface gráfica;
- **Programação Orientada a Objetos (POO)** — organização da aplicação;
- **CSV** — armazenamento/exportação de dados durante o desenvolvimento;
- **Excel/XLSX** — formato previsto para exportação dos registros;
- **Eclipse** — ambiente utilizado durante o desenvolvimento.

---

## ⚙️ Funcionalidades

Entre as funcionalidades projetadas e desenvolvidas durante o projeto estão:

- autenticação de usuário;
- cadastro de pessoas atendidas;
- registro de informações dos atendimentos;
- armazenamento local dos dados;
- visualização dos registros;
- resumo das entradas realizadas;
- geração de informações para acompanhamento;
- exportação de dados em CSV;
- exportação para Excel.

---

## 👥 Experiência do Usuário

Um dos requisitos identificados durante a visita à instituição foi a necessidade de desenvolver uma aplicação **simples, prática e intuitiva**.

Como o sistema seria utilizado também por pessoas com menor familiaridade com tecnologia, a interface foi planejada buscando reduzir a complexidade das operações necessárias para realizar os registros.

---

## 🔄 Desenvolvimento

O projeto foi desenvolvido de maneira incremental durante a disciplina.

O processo envolveu:

1. discussão de possíveis problemas e instituições que poderiam ser atendidas;
2. análise de viabilidade das ideias;
3. contato com a instituição;
4. levantamento das necessidades do cliente;
5. visita à Casa do Povo da Rua;
6. análise dos requisitos;
7. estudo das tecnologias necessárias;
8. desenvolvimento da aplicação;
9. documentação e apresentação acadêmica.

Durante o desenvolvimento, a equipe precisou conciliar a implementação da aplicação com o aprendizado de Java e das tecnologias utilizadas.

---

## 👨‍💻 Minha Participação

O projeto foi desenvolvido em equipe.

Durante a etapa de desenvolvimento, atuei dando **suporte à implementação da aplicação**, aproveitando conhecimentos prévios relacionados à disciplina e colaborando com os demais integrantes na resolução dos problemas encontrados.

Também participei das discussões e atividades coletivas relacionadas ao planejamento e desenvolvimento do projeto.

---

## 👥 Equipe

Projeto desenvolvido por:

- Natan Euclides Vieira
- Isaque Lopes Alves
- Isaias Sousa dos Santos
- Laylson Sousa da Costa
- Pedro Vinicios

**Professor orientador:** Pedro Gabriel Calíope Dantas Pinheiro

---

## ⚠️ Limitações

O projeto foi desenvolvido dentro do contexto e do período de uma disciplina acadêmica.

Na etapa documentada no relatório, a aplicação apresentada em sala ainda utilizava armazenamento baseado em **CSV**, enquanto uma versão integrada ao **SQLite** estava sendo desenvolvida.

Além disso, a autenticação implementada era básica e não possuía mecanismos avançados de segurança, como:

- criptografia de senhas;
- gerenciamento de permissões;
- controle de acesso baseado em funções.

Por isso, o projeto deve ser entendido como um **protótipo acadêmico**, e não como um sistema pronto para utilização em produção com dados pessoais reais.

---

---

## 🎓 Contexto Acadêmico

Projeto extensionista desenvolvido em **2024** durante a graduação em **Ciência da Computação** no **Centro Universitário Estácio Ceará — Polo Parangaba**, em Fortaleza/CE.

O trabalho permitiu aplicar conhecimentos acadêmicos de **Java, Programação Orientada a Objetos, interfaces gráficas e Banco de Dados** na construção de uma solução voltada a uma necessidade social real.

---

## 📚 Aprendizados

Além do desenvolvimento técnico, o projeto proporcionou experiência com etapas que vão além da programação:

- levantamento de requisitos;
- contato com um cliente real;
- análise de necessidades;
- desenvolvimento em equipe;
- divisão de responsabilidades;
- documentação técnica;
- resolução de problemas durante o desenvolvimento;
- aplicação da tecnologia em um contexto social.

O projeto demonstrou, na prática, como conhecimentos adquiridos durante a graduação podem ser utilizados para desenvolver soluções tecnológicas voltadas a **problemas e necessidades reais da sociedade**.