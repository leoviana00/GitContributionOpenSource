## Contribuindo para o Projeto

[![Star](https://img.shields.io/github/stars/leoviana00/GitContributionOpenSource?style=social)](https://github.com/leoviana00/GitContributionOpenSource/stargazers)
[![Forks](https://img.shields.io/github/forks/leoviana00/GitContributionOpenSource?style=social)](https://github.com/leoviana00/GitContributionOpenSource/forks)
[![GitHub Issues](https://img.shields.io/github/issues/leoviana00/GitContributionOpenSource?style=social)](https://github.com/leoviana00/GitContributionOpenSource/issues/)

👍 Primeiramente, obrigado por dedicar um tempo para contribuir! 🎉👍

Este projeto adere ao [código de conduta](https://github.com/leoviana00/GitContributionOpenSource/blob/main/CODE_OF_CONDUCT.md). Ao participar, espera-se que você cumpra este código.
O projeto foi criado para fins educacionais , tendo como objetivo principal praticar a a contribuição em projetos.
Alem disso, praticar abertura de issues, pull-requests, configuração e utilização de issues templates, padronização de commits e branchs. Então sinta-se livre para contribuir. 

Formas de contribuição:

❗ Resolvendo, respondendo ou indicando **issues**

📄 Realizando uma alteração no arquivo `contribution_project` através de um **fork**

⭐ Adicionando aos favoritos (**star**)

> [!IMPORTANT]
> A seguir, você pode encontrar algumas coisas para manter em mente antes de contribuir:

1. [Issues](#issues)
2. [Commits](#commits)
3. [Lista de commits permitidos](#lista-de-tipos-de-commits-permitidos)
4. [Branches](#branches)
5. [Pull Requests](#pull-requests)
6. [Praticando a contribuição com projetos](#contribuição)

## Issues

Para abertura de issues, podem ser seguidos doi modelos ja estabelecidos em template:

1. Em casos de report de bug, utilizar o template: [Template - BUG REPORT](.github/ISSUE_TEMPLATE/bug_report.md)
2. Em casos de Solicitação de uma nova funcionalidade, uma sugestão em si, utilizar o template: [Template - FEATURE REPORT](.github/ISSUE_TEMPLATE/feature_request.md)


O título da issue deve-se seguir o modelo sugerido no template - Exemplo:
```
[BUG] - Título do bug
[SUGESTÃO] - Título da sugestão
```
> [!TIP]
> Se o problema for fechado sem desenvolvimento, use um dos rótulos abaixo:

- `wontfix`
- `invalid`
- `duplicate`

> [!NOTE]
> Em casos onde você trabalhou na solução de uma issue:
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

### Criação de branchs

- Se quiser criar o branch e ao mesmo tempo já trocar para ele, pode usar:

```bash
git checkout -b novobranch
```
- e quiser criar o branch a partir de outro existente (não necessariamente o atual):

```bash
git checkout -b novobranch branch_existente
```

- Trocar para uma outra branch

```bash
git checkout NovaBrach
```

- Verificar branchs existentes

```bash
git branch
```


## Pull Requests

> [!NOTE]
> O corpo do PR deve conter as respostas baseadas no [pull-request template](https://github.com/leoviana00/GitContributionOpenSource/blob/main/.github/pull_request_template.md)
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
- [ ] Minha contribuição está de acordo com o [Guia de Contribuição](https://github.com/leoviana00/GitContributionOpenSource/blob/main/CONTRIBUTING.md)

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

## Contribuição

### 1 - Fork do repositório

Acesse a página principal do repositório e clique no botão "Fork" no canto superior direito da página.
Para mais informações. [Como criar um fork](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)

### 2 - Clone localmente

Comando `git clone` seguido da URL do seu fork para clonar o seu repositório localmente. 
Por exemplo:

- Em seguida, adicione seu fork como um projeto local:

```bash
git clone https://github.com/SEU_USERNAME/GitContributionOpenSource.git
```
Pressione enter, e uma cópia do seu fork no GitHub será criada localmente.
Para mais informações [Clonar repositório localmente](https://docs.github.com/pt/repositories/creating-and-managing-repositories/cloning-a-repository)
Um pouco mais sobre repositórios remotos: [About remote repositories](https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories)

- Em seguida, vá para sua pasta local
```bash
cd GitContributionOpenSource
```

- Adicionar controles remotos git:

```bash
git remote add fork https://github.com/YOUR-USERNAME/GitContributionOpenSource.git
git remote add upstream https://github.com/leoviana00/GitContributionOpenSource.git
```

- Agora você pode verificar se tem seus dois controles remotos git:

```bash
git remote -v
```

- Com o objetivo de se manter atualizado com o repositório central:

```bash
git pull upstream main
```

### 3 - Criar uma **branch** 
Comando para criação de branch

```bash
git checkout -b feature-contribuicao
```
S
>[!IMPORTANT]
>Para criar e alternar para a nova branch siga as orientações de [`Criação de branchs`](#branches)

### 4 - Alteração de um arquivo

Na raiz do projeto abra o arquivo [contribution_project](https://github.com/leoviana00/GitContributionOpenSource/blob/main/contribution_project.md) e adicione uma linha:
Exemplo: `**Testing PR NUMERO QUALQUER**` e feche o arquivo.

### 5 - Adicione suas alterações à "staging area" 

Comando:

```bash
git add contribution_project.md
```
Para mais informações sobre [Staging Area](https://petcomputacaoufrgs.github.io/intro-ao-git/staging-area.html)

### 6 - Crie um Commit
Crie um commit e adicione a mensagem indicando a alteração realizada:
```bash
git commit -m "docs(contribuicao): Update do arquivo contribuition_project"
```
>[!IMPORTANT]
> Verifique o bloco de  [`Commits permitidos`](#lista-de-tipos-de-commits-permitidos) para escrever a mensagem do seu commit de forma clara e padronizada.

### 7 - Envie as Alterações
Envie as alterações realizadas no seu repositório local para a branch `feature-contribuicao` no seu repositório remoto com o comando:
```bash
git push origin feature-contribuicao
```

### 8 - Crie um **Pull Request**.

Atente-se para a seguir as orientações para a contribuição, principalmente:
- Seu PR deve modificar apenas o arquivo contribution_project.md (dê uma olhadinha na aba "Files changed");
- O título do commit deve atender a definição de nomenclatura descrita em [`Lista de commits permitidos`](#lista-de-tipos-de-commits-permitidos).

>[!NOTE]
> Caso não saiba como criar uma solicitação de pull request, siga as orientações definidas em [`Pull Requests`](#pull-requests)
