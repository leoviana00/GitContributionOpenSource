## Contribuindo para o Projeto

[![Star](https://img.shields.io/github/stars/leoviana00/GitTemplate?style=social)](https://github.com/leoviana00/GitTemplate/stargazers)
[![Forks](https://img.shields.io/github/forks/leoviana00/GitTemplate?style=social)](https://github.com/leoviana00/GitTemplate/forks)
[![GitHub Issues](https://img.shields.io/github/issues/leoviana00/GitTemplate?style=social)](https://github.com/leoviana00/GitTemplate/issues/)

👍 Primeiramente, obrigado por dedicar um tempo para contribuir! 🎉👍

Este projeto adere ao [código de conduta](https://github.com/leoviana00/GitTemplate/blob/main/CODE_OF_CONDUCT.md). Ao participar, espera-se que você cumpra este código.
O projeto foi criado para fins educacionais , praticar a abertura de issues e e pull-requests, configuração e utilização de issues templates, padronização de commits e branchs. Então sinta-se livre para contribuir. 

Formas de contribuição:

⚠️ Resolvendo, respondendo ou indicando **issues**

⭐ Adicionando aos favoritos (**star**)

> [!IMPORTANT]
> A seguir, você pode encontrar algumas coisas para manter em mente antes de contribuir:

1. [Issues](#issues)
2. [Commits](#commits)
3. [Lista de commits permitidos](#lista-de-tipos-de-commits-permitidos)
3. [Branches](#branches)
4. [Pull Requests](#pull-requests)

## Issues

Cada trabalho tem que estar relacionado a um issue. A issue terá um título ja pr-edefinido nos templates:

- [Template - BUG REPORT](.github/ISSUE_TEMPLATE/bug_report.md)
- [Template - FEATURE REPORT](.github/ISSUE_TEMPLATE/feature_request.md)

Exemplo:
```
[BUG] - Título do bug
[SUGESTÃO] - Título da sugestão
```
> [!TIP]
> Cada problema deve conter uma `label` que reflita a categoria do problema. 
> Se o problema for fechado sem desenvolvimento, use um dos rótulos abaixo:

- `wontfix`
- `invalid`
- `duplicate`

> [!NOTE]
> Quando uma tarefa for concluída, crie uma [solicitação de pull Pull Request](#pull-requests) que feche a issue.

## Commits

> [!IMPORTANT]
> O padrão a ser seguido para os commits é baseado no [conventional commit specification](https://www.conventionalcommits.org/en/v1.0.0-beta.2/). 

- Esse padrão é escrito da seguinte forma:

```
<tipo>[(escopo opcional)]: <descrição>

[corpo opcional]

[rodapé opcional]
```

| Campo     | Obrigatório | Descrição |
| --------- | ----------- | --------- |
| Tipo      |     ✅      | Tipo do commit que vai ser feito. Verificar a [lista de tipos permitidos](#lista-de-tipos-de-commits-permitidos) |
| Escopo    |     ❌      | Arquivo, domínio, ou módulo que aquele commit se refere |
| Descrição |     ✅      | Uma descrição curta sobre o commit |
| Corpo     |     ❌      | Uma descrição maior, caso não consiga explicar com clareza tudo o que tem no commit |
| Rodapé    |     ❌      | Fechamento de tarefas e/ou informação sobre breaking changes |


## Lista de tipos de commits permitidos

| Tipo de Commit | Scope        |Descrição                                                             | Exemplo
| ---------------|--------------|----------------------------------------------------------------------|-----------
| `feat`         | portfolio    | Adiciona uma nova funcionalidade ao projeto.                         | `feat(portfolio): add USENAME.md profile`
| `fix`          | cadastro     | Corrige um bug ou problema no projeto.                               | `fix(cadastro): fixed issue fix#IssueNumber`
| `docs`         | arquitetura  | Altera a documentação do projeto.                                    | `docs(arquitetura): update README.md`          
| `style`        | comunicacao  | Realiza mudanças na aparência, sem alterar a funcionalidade.         | `style(comunicacao): add EFFECTNAME to COMPONENT`
| `refactor`     | services     | Realiza mudanças no código que não alteram a funcionalidade.         | `refactor(services): refactor at CLASSNAME`
| `test`         | editarsenha  | Adiciona ou modifica testes no projeto.                              | `test(editarSenha): add unit test for UserService`
| `build`        | nfe          | Mudanças que afetam o build ou dependências exeternas (gulp, npm)    | `build(nfe): update npm`
| `ci`           | scope-a      | Mudanças na configuração da Integração Contínua (Travis, Circle)     | `ci(scope-a): remove stage tests at pipeline jenkins `
| `revert`       | scope-b      | Reversão de um commit                                                | `revert(scope-b): revert the last two commits`


- Exemplos de commits:


- Um commit com rodapé `fechando uma issue`:

```
fix(pagamento): muda a chave do RecebaSeguro

A chave que estava sendo usada era de desenvolvimento,
mas acabou sendo enviada para produção

Closes a tarefa #457
```

- Um commit com rodapé informando sobre `breaking changes`:

```
refactor(produto): remove o método #adicionarAoCarrinho

O método já tinha sido depreciado e agora foi removido

BREAKING CHANGE: o método públic #adicionarAoCarrinho foi removido
```

## Branches

> [!NOTE]
> Nomes de branches são compostos de 2 partes:

1. O type ou categoria do branch. Os types podem ser os seguintes:

- `feat`         
- `fix`          
- `docs`       
- `refactor`

2. O que o branch faz em si.

```
<tipo>-<descrição>

```
- Quadro de exemplos:

| Tipo de Commit | Descrição                                     | Exemplo
| ---------------|-----------------------------------------------|-----------
| `feat`         | Uma nova funcionalidade                       | `feat-cadastro-fornecedor`
| `fix`          | Correção de um bug                            | `fix-cadastro-clientes`
| `docs`         | Apenas mudanças de documentação;              | `docs-documentar-arquitetura`  
| `refactor`     | Mudança que não adiciona uma funcionalidade   | `refactor-edicao-colaboradores`


| Campo     | Obrigatório | Descrição |
| --------- | ----------- | --------- |
| Tipo      |     ✅      | Tipo do commit que vai ser feito. Verificar a [lista de tipos permitidos](#lista-de-tipos-de-commits-permitidos) |
| Descrição |     ✅      | O que o branch faz em si |



## Pull Requests

> [!NOTE]
> O corpo do PR deve conter as respostas baseadas no [pull-request template](https://github.com/leoviana00/GitTemplate/blob/main/.github/pull_request_template.md)
> Como criar uma solicitação de Pull Request: [Documentação](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)

- Corpo do Pull Request Template:

```md
## Descrição

Descrição da alteração que está sendo proposta.

## Tipo de alteração

- [ ] Correção de bug
- [ ] Nova funcionalidade
- [ ] Alteração na documentação
- [ ] Outro (especifique)

## Pre-merge Checklist

- [ ] Minhas alterações não deletam partes do projeto
- [ ] Minhas alterações não introduzem novos problemas
- [ ] Minha contribuição está de acordo com o [Guia de Contribuição](https://github.com/leoviana00/GitTemplate/blob/main/CONTRIBUTING.md)

## Comentários adicionais

Adicione aqui quaisquer comentários ou informações adicionais relevantes para o revisor.

Caso o PR possua relação com alguma issue aberta, usar o modelo de descrição abaixo, desse moda fechando/resolvendo a issue relacionada.

Ex: 
Closes #5
Aqui estão todas as informações adicionais necessárias para o revisor, por exemplo, execute o Yarn antes de revisar.

## Screenshots

| Before | After |
| ------ | ----- |
| Image  | Image |

```

> [!NOTE]
> Em casos no qual o `PR` tem relação cpm alguma issue:
> Em comentários adicionais, inicie com uma [mensagem que encerre as issues relacionadas ](https://docs.github.com/pt/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue) e abaixo dela, em uma nova alinha adicione quaisquer comentários ou informações adicionais relevantes para o revisor.