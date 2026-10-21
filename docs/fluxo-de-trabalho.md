# Fluxo de trabalho

## Branches

- `main` é sempre implantável.
- Branches curtas: `feat/...`, `fix/...`, `docs/...`.

## Pull requests

1. Abra o PR cedo (como draft, se necessário).
2. Descreva o **porquê**, não só o quê.
3. CI verde é pré-requisito para revisão.
4. Pelo menos 1 aprovação. Veja as regras de
   [code review](http://localhost:3000/docs/default/component/wiki-engineering/code-review/).

## Commits

Seguimos [Conventional Commits](https://www.conventionalcommits.org/):

```text
feat(api): adiciona endpoint de busca
fix(auth): corrige expiração do token
docs(runbook): documenta rollback
```

## Deploy

Merge na `main` faz o deploy automático em dev. Veja o
[pipeline padrão](http://localhost:3000/docs/default/component/wiki-golden-path/ci-cd/).
