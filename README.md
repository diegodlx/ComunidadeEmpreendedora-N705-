# ComunidadeEmpreendedora

Este projeto visa aliar o desenvolvimento de habilidades para planejamento e execução de uma aplicação com uma demanda que tenha impacto social, atendendo os objetivos de desenvolvimento sustentável no Brasil das Nacões Unidas, masi especificamente o objetivo 11 através da geração de renda preferencialmente em periferias e pequenas comunidades locais.

## Identificação, justificativa e objetivos
Por muitas vezes temos necessidades de serviços em nossa própria residência ou até mesmo de aparelhos que possuímos e não conhecemos um profissional para realização do mesmo. As necessidades são inúmeras, desde ummarceneiro para consertar ou fabricarum pequeno móvel ou até mesmo um técnico especializado para consertar o celular que quebrou a tela ao cair no chão. Normalmente a pessoa pergunta a um amigo ou familiar se conhece alguém que faça o serviço desejado porque não sabe quem pode fazer. Ainda apor cima hoje em dia é necessário que o prestador tenha boas recomendações, pois não queremos correr o risco de pagar por um serviço que deixe a desejar.
Muitas vezes esses serviço existem na própria comunidade local, comunidade religiosa ou até em um bairro de baixa renda próximo, mas devido a falta de renda ou conhecimento para divulgação ou até mesmo por ser um serviço para geração de renda extra, o prestador não consegue chegar aos clientes em potencial.
Nossa solução é para que esses serviços sejam localizados com maior facilidade e confiança, movimentando assim o empreendedorismo local de cada bairro, comunidade ou região metropolitana da cidade.

## Escopo do projeto
O presente planejamento visa o desenvolvimento de uma aplicação multiplataforma totalmente funcional e testada em ambiente controlado já pronta para entrar em produção.

## Tecnologias propostas
- React Native
- JavaScript
- Node.js
- Express
- PostgreSQL

## Visão geral da arquitetura
### Camada frontend
Responsável pela apresentação visual da aplicação, sendo uma visão para o cliente, com o foco em mostrar os prestadores e serviços oferecidos bem como a possibilidade de solicitar orçamento para um serviço já outra visão para o prestador, onde possibilita o cadastro de serviços realizados, montagem de orçamento e dados do mesmo.
### Camada backend
Proporcionando maior escalabilidade e facilidade de manutenção do código bem como visando a melhoria e facilitação de implementações futuras, será utilizada a metodologia de microsserviços onde a aplicação é dividida em vários pequenos serviços independentes, cada um responsável por uma funcionalidade específica e comunicando-se através de APIs para solicitar/enviar as informações necessárias.
Abaixo estão as descrições de cada microsserviço:
1. Microsserviço de Autenticação e Usuários:
- Gerencia o cadastro, login e autenticação de clientes e prestadores.
- Armazena dados de perfil, como nome, e-mail, foto e tipo de usuário.
2. Microsserviço de Serviços e Categorias:
- Mantém o catálogo de serviços disponíveis (ex: encanador, eletricista, limpeza).
- Gerencia as categorias e subcategorias, permitindo uma busca organizada.
3. Microsserviço de Solicitações (Propostas):
- Recebe as solicitações de serviço dos clientes, que incluem a descrição do trabalho, foto e a localização.
 - Dispara eventos para outros serviços (por exemplo, avisando a criação de uma nova solicitação).
4. Microsserviço de Propostas e Orçamentos:
- Permite que prestadores enviem orçamentos para as solicitações.
- Armazena o status de cada proposta (enviada, aceita, rejeitada).
5. Microsserviço de Notificações:
- Envia notificações push em tempo real para os aplicativos móveis.
- Notifica prestadores sobre novas solicitações e clientes sobre novas propostas.
### Camada de dados
Para esta aplicação será utilizado banco de dados relacional PostgreSQL.
### Diarama de arquitetura
<img width="585" height="345" alt="Image" src="https://github.com/user-attachments/assets/44eef1bd-aa60-4d13-bbb1-a34adac7270d" />

## Diagrama de fluxo do sistema
<img width="655" height="647" alt="Image" src="https://github.com/user-attachments/assets/6352f0d6-043d-47a0-a468-064044d491fa" />

## Cronograma para etapa 2 (N708)
<img width="388" height="900" alt="Image" src="https://github.com/user-attachments/assets/682b7988-6b7f-4961-8b1d-0b618e62d99c" />

## Integrante da equipe
Este trabalho será executado integralmente por Diego Loyola Ximenes, matrícula 2316196
