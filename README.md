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
    
- No dia 7 de outubro de 2024, O foco principal deste dia foi a implementação de melhorias na aplicação ScreenMatch, visando a otimização do back-end e a organização do código.
  - Estudo e implementação do CORS: Foi realizada uma análise detalhada sobre a importância da configuração CORS (Cross-Origin Resource Sharing) para o projeto. Essa implementação é crucial para garantir que o back-end possa aceitar requisições de diferentes origens, facilitando a comunicação entre o front-end e o back-end, especialmente em cenários onde eles operam em domínios distintos.
  - Integração do DevTools: adicionadas as dependências do DevTools ao projeto. Essa ferramenta proporcionará um ambiente de desenvolvimento mais ágil e eficiente, permitindo melhor monitoramento e depuração durante a execução da aplicação.
  - Criação do Pacote Service: Foi implementado o pacote service, que inclui a criação da classe SerieService. Essa classe foi projetada para delegar regras de negócio, melhorando a organização do código e seguindo as boas práticas de desenvolvimento. A separação de responsabilidades torna a manutenção mais simples e promove o reuso de código, contribuindo para a escalabilidade do projeto.
  - Refatoração do Método de Criação de SerieDTO: O método responsável pela criação dos objetos SerieDTO foi refatorado, com o objetivo de melhorar a legibilidade e a clareza do código. Essa melhoria facilitará futuras manutenções e colaborações.

- No dia 9 de outubro de 2024, o foco principal foi a correção de problemas e a implementação de novas funcionalidades na aplicação ScreenMatch, visando otimizar as consultas de séries e a entrega de dados detalhados.
  - Correção na Consulta de Séries Lançadas Recentemente: Após alguns testes de requisições feitas do front-end para o back-end, foi identificado um problema na consulta que trazia os dados das séries lançadas recentemente com base nas datas de lançamento dos episódios. Utilizando derived queries, a consulta apresentava inconsistências ao retornar apenas alguns dados, especialmente em casos de múltiplos episódios lançados recentemente. Para corrigir isso, foi necessário abandonar o uso de derived queries com left join e optar por uma consulta JPQL com inner join, garantindo que os dados fossem corretamente agrupados por série e que as 5 séries mais recentes fossem retornadas.
  - Implementação de Busca por ID e Episódios de Séries Específicas: Além da correção, foi implementado o método de busca por ID de uma série, permitindo que os dados detalhados de uma série específica fossem obtidos. Também foi criado o método que retorna todos os episódios de uma série específica, possibilitando que o front-end receba a lista completa de episódios referentes à série buscada.

- No dia 10 de outubro de 2024, o foco foi na implementação de novos métodos para melhorar a interação do front-end com os dados de séries e episódios na aplicação ScreenMatch.

  - Implementação de Busca de Episódios por Temporada: Foi implementado um novo método utilizando JPQL para buscar episódios relacionados a uma série específica, filtrando por temporada. Com essa melhoria, o front-end agora consegue exibir todos os episódios de cada temporada de uma série, proporcionando uma navegação mais organizada e fluida entre temporadas e seus episódios.

  - Filtragem de Séries por Gênero: Além disso, foi implementado um método para filtrar as séries por gênero, aproveitando uma funcionalidade já existente que faz o mapeamento adequado entre o gênero selecionado no front-end e o correspondente no banco de dados. Isso permitiu uma busca mais precisa e eficaz por séries com base no gênero escolhido pelo usuário.

## Conclusão
O desenvolvimento da API ScreenMatch evoluiu significativamente ao longo da formação Java Spring, incorporando diversas práticas essenciais para o desenvolvimento web moderno. A transição para uma aplicação web, a utilização de Spring Boot, e a implementação de padrões como MVC e o uso de DTOs reforçaram a estrutura do projeto, tornando-o mais modular e fácil de manter.

As melhorias implementadas, como a solução de problemas nas consultas de séries recentes, a filtragem de séries por gênero, e a busca detalhada de episódios por temporada, destacam o foco na entrega de uma API eficiente e funcional, capaz de lidar com dados complexos de maneira otimizada. Além disso, o projeto foi aperfeiçoado com a configuração de CORS e a integração de ferramentas de desenvolvimento, resultando em um fluxo de trabalho mais ágil.

Com essas evoluções, a API ScreenMatch está pronta para fornecer suporte robusto e eficiente para aplicações front-end, oferecendo uma base sólida e escalável para futuras implementações e melhorias, seja no âmbito funcional ou na experiência do usuário.

