# AWS EXPERT - LinuxTips

## Mudanca na infraestrutura

- A Infraestrutura comecou a mudar quando surgiu o conceito de devops e esse movimento se fortaleceu por conta da computacao em nuvem.

## O que eh cloud computing? 

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

SaaS - Software as a Service
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
