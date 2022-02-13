# Formação DevOps



## DevOps

### O que é DevOps?


#### Currículo com as skills mais pedida entre 2021 e 2022:

##### Linux

- Ubuntu
- Red Hat

##### Versionamento de código

- Git
- GitHub

##### Iac
- TerraForm

##### Gerência de configuração
- Ansible
- Puppet
- Chef

##### Gerenciamento de tarefas
- Rundeck 

##### CI/CD
- Gitlab
- Jenkins

##### Monitoramento
- Zabbix
- Grafana
- Prometheus

##### Container
- Docker
- Kubernetes

##### Logs
- Graylog

##### Filas
- RabbitMQ


##### Cloud

- AWS
- Azure


**Fontes:**

[Cloud Google - DevOps](https://cloud.google.com/devops/)



## Continuous Integration (CI)

### O que é Continuous Integration (CI)?

O Continuous Integration (CI) ou Integração Contínua



Ao integrar o código o tempo todo, diminui a chance de não percebermos uma falha, já que menos código foi integrado de uma vez só.

Menos código a integrar simplifica muito. Lembrando que não deve ter um evento especial para a integração e sim deve ser uma prática sólida e diária.

### Sistema de controle de versão

Em uma equipe de desenvolvimento, precisaremos de uma ajuda para sincronizar e manter o histórico do código, de maneira concreta utilizamos ferramentas como Git e SVN.

A integração contínua não possui necessidade de muitas ferramentas, em tese, mas alguns auxílios que são padrão em práticas de desenvolvimento são requiridos.

O Git é o mais popular em integração hoje em dia, mas não precisamos utiliza-lo, basta que tenhamos algum modelo de controle de versão de nossa escolha.

A ferramenta em si não importa, mas o que devemos inserir em nosso sistema de controle? De maneira geral, deve conter tudo aquilo que é necessário para a construção do projeto.

- código
- scripts
- migrações, schemas 
- IDE Configs

Os testes são uma parte essencial da aplicação. Testes também são códigos, e *scripts* relacionados a eles devem entrar no repositório.

Faz parte da aplicação e é preciso para construir e executar o projeto.

Lembre-se precisamos de uma ferramenta, como SVN ou Git, para manter o histórico e facilitar a colaboração entre desenvolvedores. Isso serve para qualquer projeto de software!

### Organização de repositórios

O que é mais natural é utilizar um repositório para cada projeto, de um tamanho razoável com escopo bem definido. Essa forma de organização é chamada **Multi-repo**.

No entanto, nos últimos anos, surgiu uma nova forma de organização dos nossos projetos dentro de repositórios. Empresas grandes de tecnologia como Google e Facebook não utilizam o esquema Multi-repo, porque são empresas que trabalham em inúmeros projetos de maneira concomitante. Empresas que atuam com outra dimensão de projetos utilizam o **Mono-repo**, ou seja, um único e gigantesco repositório que acumula todos os projetos. 

A desvantagem do segundo modelo é o repositório precisará ser realmente grande, e o build pode ser lento, talvez nem o Git seja mais a ferramenta adequada para fazer o controle de versões para esta situação. Contudo, como temos apenas um grande repositório temos uma administração relativamente mais simples, então a verificação de padrões é facilitada. A refatorações são globais, afinal estão todos dentro da mesma base. 

**Vantagens do Multi-repo**

Já que cada projeto/módulo tem o seu repositório, podemos definir as permissões por projeto!

A base de código é apenas desse projeto/módulo e não do sistema todo. Isso agiliza na hora de usar o código, pensando no *clone*, importação na IDE, no *commit* e *build* do projeto.

**Resumo até agora:**

- **Integração Contínua** (CI) significa integrar as alterações no *mainline*(*master* ou *trunk*) diariamente
- Para usar **Integração Contínua**, é necessário usar um sistema de controle de versão (VCS), e no final integramos o código no repositório (usar Git não é obrigatório)
- Aplicando **Integração Contínua** corretamente, diminuímos os problemas de integração (como *merge hell*), melhoramos a comunicação entre desenvolvedores e antecipamos a descoberta de *bugs*
- Os estilos de organização de projeto
  - **Mono-repo** possui todos os projetos em um único repositório
  - **Multi-repo** separa um repositório para cada projeto





Devido a sua importância, a **Integração Contínua** é um tópico bastante discutido na literatura e na web, veja algumas fontes: 

- Livro: Continuous Integration, de Paul M. Duvall

- Artigo da ThoughtWorks: [Continuous integration](https://www.thoughtworks.com/pt/continuous-integration)

- Artigo do Martin Fowler: [Continuous Delivery](https://martinfowler.com/bliki/ContinuousDelivery.html)

- Série de artigos da Caelum:

   

  - [Branches e integração contínua: o problema de feature branches](https://blog.caelum.com.br/branches-e-integracao-continua-o-problema-de-feature-branches/)
  - [Integração Contínua - Builds rápidos com Grids e paralelismo](https://blog.caelum.com.br/integracao-continua-builds-rapidos-com-grids-e-paralelismo/)
  - [Integração contínua: deploys e aprovações sem dor de cabeça para o cliente](https://blog.caelum.com.br/integracao-continua-deploys-e-aprovacoes-sem-dores-de-cabeca-para-o-cliente/)

- Artigo no CodeBetter: [Check in Dance](http://codebetter.com/jeremymiller/2005/07/25/using-continuous-integration-better-do-the-check-in-dance/)



**Fontes:**

- [Red Hat - Integração e entrega contínuas: pipeline CI/CD](https://www.redhat.com/pt-br/topics/devops/what-is-ci-cd)
- [Curso Alura de CI](https://www.alura.com.br/curso-online-desenvolvimento-software-integracao-continua)





## Continuous Delivery (CD)

### O que é Continuous Delivery (CD)?

O Continuous Delivery (CD) ou Entrega Contínua



**Fontes:**

- [Red Hat - Integração e entrega contínuas: pipeline CI/CD](https://www.redhat.com/pt-br/topics/devops/what-is-ci-cd)



