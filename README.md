# Java Criando uma API REST com Spring Boot Web
> Projeto desenvolvido como parte da formação Java Spring da Alura.

## 🔨 Objetivos do projeto
- Dar continuidade ao projeto Screenmatch, iniciado nos cursos anteriores da formação, [Java-SpringBoot-ScreenMatch](https://github.com/alexzxcg/Java-SpringBoot-ScreenMatch), [Java-ScreenMatch-Com-JPA](https://github.com/alexzxcg/Java-ScreenMatch-Com-JPA), evoluindo a aplicação para o Spring Boot Web;
- Criar uma API REST para conectar o back-end com um front-end desenvolvido pela Alura;
- Mapear rotas de conexão e tratar a comunicação web via controladores;
- Conhecer e tratar erros de CORS (Cross-Origin Resource Sharing), entendendo o que significa e como cada uma dessas quatro letras impacta na aplicação;
- Aplicar boas práticas no desenvolvimento web, utilizando DTOs (Data Transfer Objects) para transportar dados e services para encapsular a lógica de negócio;
- Manter o foco no desenvolvimento do Screenmatch, um aplicativo de streaming de filmes e séries, agora evoluindo para uma API moderna e eficiente.

## O que foi feito até agora?
- No dia 4 de outubro de 2024, foi realizada a iniciação do projeto com o propósito de evoluir a aplicação ScreenMatch. O foco principal dessa fase foi a transição da aplicação de um modelo de linha de comando (command line) para uma estrutura de aplicação web, permitindo uma interação mais rica e dinâmica com os usuários.
  - Refatoração do Código: O código existente foi refatorado para adequá-lo ao novo formato de aplicação web, o que inclui a reorganização das estruturas de classe e métodos.
  - Adição de Dependências: Um pacote controller foi implementado para gerenciar a aplicação segundo o padrão MVC (Model-View-Controller). Isso permitiu uma separação clara de responsabilidades, facilitando a manutenção e escalabilidade do código.
  - Implementação de DTOs: O uso de DTOs (Data Transfer Objects) foi introduzido para representar os dados fornecidos pela aplicação. A classe SerieDTO foi criada para encapsular as informações relevantes sobre as séries, facilitando a manipulação e transferência de dados entre camadas.
  - Testes de Requisições: Após as implementações, foram realizados testes nas primeiras requisições da aplicação para verificar como os dados estavam sendo fornecidos. Isso garantiu que a comunicação entre o cliente e o servidor estivesse funcionando conforme o esperado.
