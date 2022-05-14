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

- Podemos adicionar permissoes a para usuarios especificos dentro da AWS, basta clicar em (Attach existing policies directly) dentro de Add Permissions.
- Quando se cria um usuario pelo IAM, nao esquecer de configurar o MFA para este usuario, extremamente importante esse passo para a seguranca da AWS.

## Roles

- Uma role basicamente permite que recursos da AWS se comuniquem com outros recursos da AWS.
- Roles, podemos agrupar dentro de uma role varias politicas, como se fosse um grupo de politicas para facilitar a manipulacao na plataforma.
- Por exemplo, uma Role especifica pra times de desenvolvimento, onde quem tem essa role pode: Mexer com EC2, mexer com S3, SQS, algumas coisas no IAM.
- Podemos adicionar roles em uma Account(Conta), em um servico da AWS e entre outros.
- Podemos usar roles para que servicos da AWS tenha acesso a outros servicos. Exemplo: AWS EC2 ter acesso ao SQS. Ou que um LAMBDA acesse outros servicos dentro da AWS.
- Importante definir um prefixo ou sufixo para diferenciar a roles da AWS das nossas
- Para atachar uma role em um servico, navegue ate a pagina do servico, selecione e procure nas configuracoes por "Attach/Replace IAM role"

## Across Account Role

- Role entre contas da AWS, onde uma conta permite que outra determinada conta assuma o controle temporariamente.
- Podemos definir permissoes para que a conta que vai assumir nao realize todas as operacoes.
- Para sair de uma conta e ir para outra conta assumindo a role que foi setada na outra conta: Clica no nome da conta e selecione "Switch Role"
- Depois basta colocar o ID da conta de destino, o nome da Role (Cross) e assumir a conta.

## Policies (managed)

- Policy nada mais eh que permissoes que podemos dar para recursos da AWS, por exemplo, ler, editar, alterar ou remover qualquer recurso da AWS.
- Nos detalhes de uma policy, podemos ver suas versoes, quem esta usando essa policy e entre outras coisas.
- Existem varias policies da AWS e podemos utiliza-las para falicitar nossa vida dentro da AWS.
- Quando estiver com duvida do que a Policy faz, basta olhar os detalhes da policy e ver o que ela permite e nao permite para os recursos que ela for atachada.

## Create Policies

- Clique em criar policies
- (Service) - Escolha o servico -> EC2, RDS, IAM e etc.
- (Actions) - Selecione o que podera fazer nesse recurso, ler, escrever, listar e etc
- (Resources) - Escolher de podera ver em todos os servicos que ja estao criados ou apenas em um recurso especifico (ARN - Amazon Resource Name).
- Quando colocamos um servico especifico, podemos escolher a regiao, a account e o nome do cluster (No caso de EKS).
- Podemos colocar algumas condicoes especificas, por exemplo: somente se houver MFA.
- Sempre bom ficar atento em como os JSON da policies sao gerados, geralmente esse assunto cai em prova, tanto para validar um json, quanto para escrever.
- A versoes da policies sao salvas, ou seja, as alteracoes feitas nela ficam registradas em (Policy versions), isso permite selecionar a versao anterior caso aconteca alguma merda ou algo do tipo.
- Para atachar uma policy, basta selecionar o recurso que voce quer (Role, UserGroups ou users) e atachar a policy.

## Identity Providers

- Podemos integrar nossa conta AWS com um AD, ou um (SSO)Single Sign On.
- Podemos criar um identity provider, basta clicar em Add provider.

## Account Settings

- Podemos definir politicas de senhas, como por exemplo: Utilizar 128 caracteres, letras maiusculas ou minusculas, alfanumericos e etc. Com isso todos os usuarios criados no IAM para essa conta vao ter que seguir essas politicas de senha.
- Security Token Service (STS) - Sao token para utilizar a AWS via linha de comando, podemos definir as regioes que esses token funcionam, podemos permitir ou nao o acesso nessas regioes via STS.

## Reports

- Mostra um relatorio das credenciais e de cada usuario dentro do IAM. Exemplo: Quando alterou a senha, se o MFA esta ativo e etc.
- Com esse relatorio podemos criar alertas, ver a saude dessas credenciais, via alguma linguagem de programacao ou qualquer outra ferramenta.

## LINKS UTEIS

- [AWS IAM Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [Access keys best practices](https://medium.com/@ashishrajan/aws-security-best-practices-access-keys-cloudsecurity-facb20aa0db6)
- [AWS CLI](https://aws.amazon.com/cli/)
