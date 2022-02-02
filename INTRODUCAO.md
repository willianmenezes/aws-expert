# AWS EXPERT - LinuxTips

## Mudanca na infraestrutura

- A Infraestrutura comecou a mudar quando surgiu o conceito de devops e esse movimento se fortaleceu por conta da computacao em nuvem.

## Dia 01 - O que eh cloud computing? 

### Principais caracteristicas:

- Agilidade
    Conseguir lancar as coisas rapido.
    
- Manutencao
    Nao e mais responsabilidade da infra cuidar de infraestrutura fisica. Fica de responsabilidade do provedor.
    
- Confiabilidade
    A confiabilidade nos nossos servicos aumenta, por conta que empresas estao trabalhando fortemente focadas em fornecer um servico de nuvem de qualidade.

- Seguranca
    Servicos de nuvem fornecem diversas funcionalidades e ferramentas de seguranca fisica (Nao precisamos nos preocupar mais), e focamos em problemas mais especificos (da nossa aplicacao).

- Performance
    Conseguimos ter muito mais performance, mas isso tem um custo. Podemos usar nossos servicos por demanda.

- Escalabilidade
    Podemos aumentar e diminuir os nossos recursos sob demanda. Ou seja, podemos escalar nossos recursos de forma facil e agil.

- Custo e elasticidade
    Saber utilizar e gerenciar os recursos sob demanda, diminuindo ou aumentando os meus custos. 
    
    Elasticidade nao quer dizer que os recursos sao infinitos, ou seja, ela tem um limite. 
    Softlimit - Pode ser alterado
    Hardlimit - Nao pode ser alterado

## O que eh cloud segundo o NIST (The national Institute of Standart and Technology)

- Ter um servico sob demanda (criar quando precisar)
- Ter acesso a uma rede distribuida
- Ter um pooling/catalogo que funcionalidades e servicos que voce pode escolher utilizar.
- Rapida elasticidade (crescer e diminuir)
- O servico precisa dar a opcao de ser medido (Tirar metricas dos seus servicos e funciondalides)

## Modelos de Cloud

Cloud nao eh apenas vender uma maquina virtual, existem varios modelos de cloud, e alguns deles sao:

- IaaS - Infraestructure as a service
    Eu nao tenho uma insfraestrutura instalada, mas quando eu preciso de algum produto (Banco de dados, VM e etc) eu posso solicitar isso a algum provedor de nuvem que trabalhe com esse modelo.

- PAAS - Platform as a Service
    Nao precisamos nos preocupar com o que esta rodando por tras das nossas aplicacoes (VM, Infra e etc), um exemplo classico disse eh a heroku.

- SaaS - Software as a Service
    Nos preocupamos em apenas utilizar os programas ou funcionalidades do provedor, como por exemplo o Microsoft 365.

- FAAS - Functions as a Service
    A ideia de um produto muito mais granular, a ideia eh deixar os servicoes bem pequenos e disponibilizar isso em uma function (por exemplo um servico de email)

## Modelos de Deploy

- Private Cloud
    Montei um servico de cloud privado, onde nenhuma outra empresa tenha acesso as ferramentas e funcionalidades que foram criadas. 

- Public Cloud
    Qualquer pessoa pode usar, AWS, Google Cloud e Azure. Voce contrata e pode comecar a acessar os recursos da plataforma.

- Hybrid Cloud
    Voce pode ter o private e public que voce utiliza, um pedaco da aplicacao esta rodando em cloud publica e outro rodando no modelo privado.

- MultiCloud
    Poder rodar suas aplicacoes em varios players de cloud.

## Dia 02 - Fundacao 

Como a gente faz pra comecar a criar as coisas na nuvem? Quais sao as melhores praticas para computacao em nuvem? 

Vamos planejar e pensar em como usar cloud computing da melhor maneira.

Nao podemos apenas criar uma conta e sair criando servicos dentro dessa conta, vamos aprender como criar a fundacao como se estivessemos no mundo real.

### Root Account

- Eh a conta principal, responsavel por todos os recursos que temos na AWS.
- Pra que serve? Iniciar e gerencias novas conta dentro da AWS, e tambem nos ajuda com o billing.
- Nao usamos a root account para criar recursos, nao eh uma boa pratica se tratando de aplicacoes de "mundo real", que vai para a producao. O correto seria utilizar sub-accounts.

### O que eh unidade Organizacional? 

- Usadas para organizar a administrar as contas, e aplicar regras separadas, contas como (DEV, QA, PROD).
- Podemos criar OU (Unidade Organizacional) por empresas,  se for o caso.
- OU (Unidade Organizacional) por departamentos (RH, Contabil, TI).
- Podemos aplicar regras separadas em cada OU (Unidade Organizacional), exemplo: Tamanho de maquinas, bloquear regioes.
- OU (Unidade Organizacional) eh uma forma de categorizar nossas contas.
- Usar OU (Unidade Organizacional) eh uma boa pratica para trabalhar com OU.
- A ideia de organizar as contas eh poder ganhar alguns poderes, podendo aplicar regras muito melhores e complexas.

### Contas AWS (Sub contas)

- Basicamente eh uma conta, igual a root account, mas com a responsabilidades de rodar servicos (EC2, Lambdas e etc)
- Podemos criar contas via invite, que ficam relacionadas com as root accounts.
- Para criar contas precisamos obrigatoriamente de nome e e-mail.
- Geramente eh colocado um email fake para criar as contas, ou coloca o email de uma pessoa da empresa (nao recomendado).
- Eh importante criar uma conta real e ler os email, senao a AWS comeca a abaixar o score.
- Cada conta criada tem um gerenciador de identidade (IAM).

### Criando contas na AWS

- Acessar o site [https://aws.amazon.com/](AWS) e clicar em criar uma conta.
- Existem um modelo chamado Free-Tier, que sao produtos que podemos usar de forma gratuita por um ano, a nao ser que passe o limite.
- Temos que tomar cuidado com os produtos que esta dentro do free tier.

### Credencias de seguranca

- Para localizar o ID da conta basta clicar em Account identifier.
- Nao esquecer de ativar o MFA.

## Criando organizacao

- Importante cadastrar os contatos de Billing, Operations e Security. Para que a amazon possa entrar em contato quando necessario sobre algum desses itens.
- Para criar uma nova organizacao, basta apenas clicar no nome de usuario no canto superior direito e clicar em Organization.
- Depois, seleciona a conta root -> clique em actions -> Create new -> Colocar o nome da organizacao -> Create organizational unit.

