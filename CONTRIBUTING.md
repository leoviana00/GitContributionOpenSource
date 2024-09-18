## Contribuindo para o Projeto

👍 Primeiramente, obrigado por dedicar um tempo para contribuir! 🎉👍

Este projeto foi feito criado para fins educacionais , praticar a abertura de issues e e pull-requests, utilização de templates, padronização de commits e branchs. Então sinta-se livre para contribuir. 

Formas de contribuição:

⚠️ Resolvendo, respondendo ou indicando issues

⭐ Adicionando aos favoritos (star)

> [!IMPORTANT]
> A seguir, você pode encontrar algumas coisas para manter em mente antes de contribuir:

1. [Issues](#issues)
2. [Commits](#commits)
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

> [!TIP]
> Esse padrão é escrito da seguinte forma:

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

- `feat`: Uma funcionalidade
- `fix`: Um ajuste de erro/bug
- `docs`: Modificação na documentação
- `style`: Mudança de estilo (ponto, vírgula, indentação)
- `refactor`: Mudança de código que não adiciona funcionalidade ou arruma um erro
- `perf`: Mudança que altera performance
- `test`: Novos testes ou correção de antigos
- `build`: Mudanças que afetam o build ou dependências exeternas (gulp, npm)
- `ci`: Mudanças na configuração da Integração Contínua (Travis, Circle)
- `chore`: Outras mudanças que não são nos arquivos de src ou test
- `revert`: Reversão de um commit

- Exemplos de commits:

- Um commit simples, sem rodapé:

```
feat(cadastro): adiciona integração com Gugou Sign-in
```

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

- `docs`: apenas mudanças de documentação;
- `feat`: uma nova funcionalidade;
- `fix`: a correção de um bug;
- `perf`: mudança de código focada em melhorar performance;
- `refactor`: mudança de código que não adiciona uma funcionalidade e também não corrigi um bug;
- `style`: mudanças no código que não afetam seu significado (espaço em branco, formatação, ponto e vírgula, etc);
- `test`: adicionar ou corrigir testes.

2. O que o branch faz em si.


```
<tipo>-<descrição>

```


| Campo     | Obrigatório | Descrição |
| --------- | ----------- | --------- |
| Tipo      |     ✅      | Tipo do commit que vai ser feito. Verificar a [lista de tipos permitidos](#lista-de-tipos-de-commits-permitidos) |
| Descrição |     ✅      | O que o branch faz em si |

> [!WARNING]
> Sempre separados por `hífen`.

> [!TIP]
> Exemplos de utilização:

```
feat-cadastro-veiculos
refactor-edicao-colaboradores
fix-busca-checklists
```

## Pull Requests

> [!NOTE]
> Um PR tem que fechar pelo menos um problema e, de preferência, apenas um. Quanto menor a quantidade de trabalho em um PR, mais fácil é revisá-lo.

O corpo do PR deve começar com uma [mensagem que encerre as issues relacionadas ](https://docs.github.com/pt/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue) e a descrição real em novas linhas.

O histórico de confirmações em um PR não deve conter  `Merge` confirmações e deve ser rebaseado em cima de`master`.

É mais fácil revisar o PR se você rebasear seus commits para que cada commit represente uma subparte do desenvolvimento e possa ser revisado de forma independente ou uma lista clara dos recursos naquele branch.

Exemplo:
```
Closes #123

Aqui estão todas as informações adicionais necessárias para o revisor, por exemplo, execute o Yarn antes de revisar.
```

- [Template Pull Request](.github/pull_request_template.md)

### Checks

Cada RP precisa ser revisado antes de poder ser mesclado.