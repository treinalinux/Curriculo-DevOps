# Infraestrutura

DevOps

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
