# Arquitetura

## Camada Frontend:
Responsável pela apresentação visual da aplicação, sendo uma visão para o cliente, com o foco em mostrar os prestadores e serviços oferecidos bem como a possibilidade de solicitar orçamento para um serviço já outra visão para o prestador, onde possibilita o cadastro de serviços realizados, montagem de orçamento e dados do mesmo.
## Camada Backend:
Proporcionando maior escalabilidade e facilidade de manutenção do código bem como visando a melhoria e facilitação de implementações futuras, será utilizada a metodologia de microsserviços onde a aplicação é dividida em vários pequenos serviços independentes, cada um responsável por uma funcionalidade específica e comunicando-se através de APIs para solicitar/enviar as informações necessárias.
Abaixo estão as descrições de cada microsserviço:
1.	Microsserviço de Autenticação e Usuários:
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

## Camada de dados:
Para esta aplicação será utilizado banco de dados relacional PostgreSQL.

## Diarama de arquitetura
<img width="585" height="345" alt="Image" src="https://github.com/user-attachments/assets/44eef1bd-aa60-4d13-bbb1-a34adac7270d" />
