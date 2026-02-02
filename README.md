📊 FlowControl (FWC) - Gestão Financeira Pessoal
O FlowControl é uma plataforma robusta de gerenciamento financeiro pessoal desenvolvida em Java com o framework Spring Boot. O projeto combina uma interface moderna e intuitiva em HTML/CSS (Thymeleaf) com uma arquitetura de back-end sólida, permitindo que usuários controlem suas receitas e despesas de forma categorizada e segura.

O objetivo principal deste projeto foi aplicar conceitos avançados de Programação Orientada a Objetos (POO) e padrões de arquitetura de software em um ecossistema Spring real.

✨ Funcionalidades Principais
A plataforma foca na experiência do usuário e na clareza dos dados financeiros:

Autenticação e Sessão: Sistema de cadastro de novos usuários e login com gerenciamento de sessão via HttpSession.

Painel de Transações: Visualização clara de todas as movimentações financeiras.

Gestão de Movimentações: Criação e exclusão de transações com atributos de Nome, Valor, Tipo (Renda/Despesa), Categoria e Prioridade.

Cálculo de Saldo Dinâmico: O sistema processa automaticamente o saldo total do usuário com base nas entradas e saídas.

Filtragem Inteligente: Capacidade de filtrar transações por tipo para uma análise mais detalhada.

Design Responsivo: Interface com cards arredondados e feedback visual (saldo em vermelho para valores negativos).

🛠️ Tecnologias e Ferramentas
Linguagem: Java 21.

Framework: Spring Boot 4.0.2.

Template Engine: Thymeleaf para renderização dinâmica do front-end.

Persistência: Arquivos JSON (Jackson ObjectMapper) para armazenamento de dados sem necessidade de banco de dados externo.

Build & Dependências: Maven.

🚀 Como Executar o Projeto
Pré-requisitos
Java 21 ou superior.

Maven instalado (ou uso do mvnw incluso).

Passos
Clone o repositório:

Bash
git clone https://github.com/seu-usuario/flowcontrol.git
cd flowcontrol
Compile o projeto:

Bash
./mvnw clean install
Execute a aplicação:

Bash
./mvnw spring-boot:run
Acesse no navegador: http://localhost:8082 (ou a porta configurada no seu log).

🧠 Arquitetura e Decisões de Projeto
O projeto segue o padrão MVC (Model-View-Controller), garantindo a separação de responsabilidades:

Model: Classes que representam as entidades do sistema, como Usuario e Transacao, utilizando Enums para Categorias e Prioridades.

View: Templates HTML utilizando Thymeleaf localizados em src/main/resources/templates.

Controller: Gerencia as rotas e a comunicação entre o usuário e o sistema (UsuarioController e TransacaoController).

Service: Camada de lógica de negócio (ex: cálculo de saldo e validação de e-mail) isolada dos controladores.

Repository: Implementação customizada de persistência em arquivos JSON utilizando Jackson, garantindo que os dados sejam salvos permanentemente em flowcontrol-data/.

Conceitos de Orientação a Objetos Aplicados
Encapsulamento: Uso de atributos privados e métodos getters/setters nas entidades de modelo.

Abstração: Representação de transações financeiras e usuários através de classes estruturadas.

Injeção de Dependência: Uso do contêiner Spring para gerenciar as instâncias de Services e Repositories através de construtores.

👨‍💻 Equipe Responsável
Silas Santos da Silva (Desenvolvedor Principal)

Estudante de Sistemas de Informação - Universidade Federal de Sergipe.

Observação: Este projeto é uma atividade acadêmica desenvolvida para consolidar conhecimentos em desenvolvimento Web com Java e Spring Boot no período de 2026.1.
