# 📊 FlowControl (FWC) - Gestão Financeira Pessoal

O **FlowControl** é uma plataforma completa para gerenciamento de finanças pessoais, desenvolvida em Java com o framework Spring Boot. O projeto permite que usuários gerenciem suas receitas e despesas com foco em usabilidade e clareza visual, utilizando uma interface moderna com elementos de *Glassmorphism*.

O principal objetivo deste projeto foi aplicar de forma prática os conceitos de **Programação Orientada a Objetos (POO)** e a arquitetura **MVC** em um sistema de controle de fluxo de caixa funcional.

---

## ✨ Funcionalidades Principais

A plataforma oferece uma interface intuitiva para o controle financeiro diário:

* **Autenticação de Usuários:** Sistema completo de cadastro e login com gerenciamento de sessão via `HttpSession`.
* **Gestão de Transações:** Permite criar, listar e excluir movimentações financeiras.
* **Categorização e Priorização:** Cada transação possui tipo (Renda/Despesa), categoria (Alimentação, Lazer, Salário, etc.) e nível de prioridade.
* **Painel de Saldo Dinâmico:** Visualização do saldo total calculado em tempo real, com feedback visual (saldo em vermelho para valores negativos).
* **Filtros Avançados:** Opção para filtrar a visualização por tipo de transação (apenas entradas ou apenas saídas).

---

## 🧠 Arquitetura e Decisões de Projeto

O projeto utiliza o padrão arquitetural **MVC (Model-View-Controller)**, separando as responsabilidades de forma modular:

### Camadas do Sistema
* **Model:** Representa as entidades e a estrutura dos dados (ex: `Usuario.java`, `Transacao.java`).
* **View:** Interface de apresentação desenvolvida em HTML5 e CSS3, utilizando **Thymeleaf** para renderização dinâmica dos dados.
* **Controller:** Atua como intermediário, processando as requisições do usuário e coordenando as respostas (ex: `UsuarioController.java`, `TransacaoController.java`).
* **Service:** Camada que contém a lógica de negócio, como validação de e-mail e cálculo de saldos (ex: `UsuarioService.java`, `TransacaoService.java`).

### Persistência de Dados em JSON
Para simplificar o ambiente de execução e evitar a necessidade de bancos de dados externos complexos, a persistência foi implementada através de arquivos JSON:
* **Mecanismo:** Utiliza a biblioteca **Jackson** para serialização e desserialização de objetos.
* **Repositórios:** As classes `UsuarioRepository` e `TransacaoRepository` gerenciam a leitura e escrita automática nos arquivos localizados na pasta `flowcontrol-data/`.

### Conceitos de Orientação a Objetos (OO)
* **Encapsulamento:** Proteção dos dados através de atributos privados e métodos getters/setters.
* **Injeção de Dependência:** O Spring gerencia automaticamente as instâncias dos serviços e repositórios, reduzindo o acoplamento.

---

## 🛠️ Como Executar o Projeto

### Pré-requisitos
* **Java 21** ou superior.
* **Apache Maven**.

### Passos para execução
1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/seu-usuario/fwc.git](https://github.com/seu-usuario/fwc.git)
   cd fwc
   
2. **Compile o projeto:**
   ```Bash
   mvn clean install
   
3. **Execute a aplicação:**
   ```Bash
   mvn spring-boot:run

4. **Acesse a plataforma:** Abra o navegador em: http://localhost:8082

---

## 👨‍💻 Equipe Responsavel

* **Silas Santos da Silva**
* **Observação: Este projeto é uma atividade acadêmica realizada para a disciplina de Sistemas de Informação/Programação, focada no desenvolvimento de aplicações web robustas com Spring Boot.**

