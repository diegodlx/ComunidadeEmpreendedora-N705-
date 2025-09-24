# Apis

As APIs e interfaces de comunicação são essenciais para conectar os diferentes componentes de uma aplicação com arquitetura de microsserviços. A definição a seguir detalha as interfaces, abrangendo a comunicação entre o frontend e o backend, e a comunicação interna entre os microsserviços. 
1. Autenticação
- POST /auth/login: realiza o login do usuário.
- GET /perfis/{id}: obtém os dados de um perfil de usuário.
2. Serviços e Categorias 
- GET /servicos: Lista todas as categorias de serviços.
3. Solicitações
- POST /solicitacoes: o cliente cria uma solicitação de serviço.
- GET /solicitacoes/{id}: obtém os detalhes de uma solicitação específica.
- PUT /solicitacoes/{id}: atualiza o status ou detalhes de uma solicitação.
- GET /clientes/{id}/solicitacoes: lista as solicitações de um cliente. 
4. Orçamentos
- POST /solicitacoes/{id}/orcamentos: o prestador envia uma proposta para uma solicitação.
- GET /solicitacoes/{id}/orcamentos: lista as propostas de uma solicitação.
- PUT /orcamentos/{id}/aceitar: o cliente aceita uma proposta.
- PUT /orcamentos/{id}/rejeitar: o cliente rejeita uma proposta.
- GET /prestadores/{id}/orcamentos: lista os orçamentos enviados por um prestador.
5. Avaliações
- POST /avaliacoes: o cliente avalia um serviço e um prestador.
- GET /prestadores/{id}/avaliacoes: lista as avaliações de um prestador.

## Interface de comunicação entre serviços
A comunicação interna entre os microsserviços será de forma síncrona (via chamadas REST). 
Os microsserviços podem fazer chamadas REST uns aos outros para obter dados necessários. Por exemplo, Orçamentos pode chamar o Solicitações para buscar os detalhes de uma solicitação.

