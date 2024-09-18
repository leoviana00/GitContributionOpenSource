name: Bug Report
description: Uma descrição clara e concisa do que é o bug.
title: "[BUG]: "
labels: "bug :beetle:"
assignees: ''
body:
- type: checkboxes
  attributes:
    label: Preflight Checklist
    description: Certifique-se de ter concluído todos os itens a seguir.
    options:
      - label: Eu li [Contributing Guidelines](../../CONTRIBUTING.md) para esse projeto.
        required: true
      - label: Eu concordo em seguir o [Code of Conduct](../../CODE_OF_CONDUCT.md) que este projeto segue.
        required: true
      - label: Eu procurei o [issue tracker](https://github.com/leoviana00/lab-k8s-prep-cks/issues) para uma solicitação de recurso que corresponde àquela que desejo registrar, sem sucesso.
        required: true