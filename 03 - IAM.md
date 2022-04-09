# AWS EXPERT - LinuxTips

### Identity and Access Management (IAM)

- Produto que ajuda na gestao de identidade em nossa conta/organizacoes.
- Podemos criar uma URL propria da nossa organizacao, para que os usuario criados via IAM possam acessar nossa organizacao por essa URL.
- Nessa url, tambem podemos definir um ALIAS para a nossa Account ID.

### User groups

- Podemos ter varios grupos, por exemplo: desenvolvimento, financeiro, qa e etc.
- Servem para colocar permissoes iguais para o mesmo grupo de usuarios.
- Podemos utilizar varios policies criadas pela amazon, bastan analisar e atachar o recurso no grupo de usuario.
- Para atachar uma policy em um grupo ja criado, basta ir em Policies e clicar em atachar a policy no grupo ou usuario desejado.
- Para remover uma policy de um grupo, basta clicar na policy e remove-la.
- E uma boa praticar deixar uma policy readonly no grupo, se por um acaso tiver algum problema deixa apenas a readonly, assim os usuarios do grupo vao conseguir pelo menos acessar os recursos.

### Users

- Esses usuarios criados no IAM vao ser usados para acessar com aquela URL personalizada da nossa conta.
- **Access key - Programmatic access:** Usuario que tem uma chave secreta, uma chave de acesso. Comumente chamado de usuario de servico, usado por aplicacoes para acessar recursos da AWS.
- Quando for criar um usuario de servico, eh uma boa pratica identificar que esse usuario eh utilizado somente por aplicacoes.
- **Password - AWS Management Console access:** Usuario que acessa via console os recursos da AWS.
- No momento da criacao do usuario, podemos colocar ele em um grupo, podemos adicionar policy.
- **Tags:** Marcacao utilizada para ajudar a identificar recursos, podemos marcar as coisas com tags para ajudar em buscar e relatorios dentro da AWS. Tambem pode ser utilizado para gerar relatorios de custos a partir das tags.

## Users - Adicionando permissoes para um usuario especifico
