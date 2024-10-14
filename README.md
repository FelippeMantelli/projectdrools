Sistema de Validação de CNH usando Drools
Este é um aplicativo simples em Java, desenvolvido para validar a Carteira Nacional de Habilitação (CNH) utilizando Drools, um motor de regras para automatizar lógicas de negócios complexas. O aplicativo verifica condições e regras relacionadas à validade de uma CNH, incluindo idade, tipo de habilitação, data de vencimento, entre outros, com base em regras pré-definidas.

Índice
Introdução
Tecnologias Utilizadas
Instalação
Uso
Estrutura do Projeto
Como Funciona
Regras Drools
Contribuição
Licença
Introdução
O objetivo deste projeto é demonstrar como utilizar o motor de regras Drools para validar CNHs no Brasil. O sistema verifica diversos aspectos da CNH para determinar se a carteira de motorista é válida. O Drools auxilia no gerenciamento das regras complexas associadas a essas validações, tornando o sistema fácil de ser expandido e modificado.

Tecnologias Utilizadas
Java 11 ou superior
Drools (Sistema de Gerenciamento de Regras de Negócios)
Maven (para gerenciamento de dependências)
JUnit (para testes unitários)
Instalação
Pré-requisitos
Antes de rodar este projeto, certifique-se de ter os seguintes itens instalados:

Java 11 ou superior
Maven
Passos para Instalação
Clone o repositório:

bash
Copiar código
git clone https://github.com/seu-usuario/sistema-validacao-cnh.git
Acesse o diretório do projeto:

bash
Copiar código
cd sistema-validacao-cnh
Instale as dependências usando Maven:

bash
Copiar código
mvn clean install
Uso
Para rodar o sistema, execute o comando abaixo:

bash
Copiar código
mvn exec:java -Dexec.mainClass="com.exemplo.CNHValidationApp"
O sistema irá executar a validação de uma CNH conforme as regras definidas no arquivo de regras Drools.

Estrutura do Projeto
A estrutura do projeto segue o padrão Maven, com os principais diretórios sendo:

bash
Copiar código
src/
│
├── main/
│   ├── java/
│   │   └── com/exemplo/
│   │       └── CNHValidationApp.java
│   ├── resources/
│       └── rules.drl
│
└── test/
    └── java/
        └── com/exemplo/
            └── CNHValidationAppTest.java
CNHValidationApp.java: Classe principal que inicia a validação da CNH.
rules.drl: Arquivo de regras Drools contendo as condições para validar a CNH.
CNHValidationAppTest.java: Testes unitários para garantir o funcionamento correto da aplicação.
Como Funciona
O aplicativo carrega os dados de uma CNH (número de registro, data de nascimento, categoria da habilitação, validade, etc.) e verifica se a CNH atende a todas as regras definidas. As regras são processadas utilizando o motor Drools, que decide se a CNH é válida ou inválida com base nas regras cadastradas.

Regras Drools
As regras Drools são definidas no arquivo rules.drl. Aqui estão alguns exemplos de regras implementadas:

Validade da CNH: Verifica se a data de vencimento da CNH já passou.
Idade mínima: Verifica se o titular da CNH tem idade suficiente para a categoria especificada.
Categoria: Verifica se a categoria da CNH é compatível com o veículo conduzido.
Você pode facilmente adicionar ou modificar essas regras no arquivo rules.drl para atender a novas necessidades.

Contribuição
Se você deseja contribuir com o projeto, fique à vontade para abrir um pull request ou reportar problemas na seção de issues.

Licença
Este projeto está licenciado sob a Licença MIT.
