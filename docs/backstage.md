# Usando o Backstage

O Backstage é o portal do desenvolvedor: catálogo de software + documentação.

## Catálogo

- **Components**: serviços, sites, bibliotecas e documentações.
- **APIs**: contratos (OpenAPI etc.) ligados aos serviços que os expõem.
- **Systems**: agrupam componentes relacionados.
- **Groups**: times donos dos componentes.

## Docs (TechDocs)

| Tipo | Onde fica | Como acessar |
|------|-----------|--------------|
| Doc de serviço | `docs/` no repo do serviço | Aba **Docs** do componente |
| Wiki | Repo próprio, `type: documentation` | Menu **Docs** → filtrar por tag `wiki` |

## Adicionar docs ao seu serviço

1. Crie `mkdocs.yml` e `docs/index.md` na raiz do repo.
2. Adicione a anotação no `catalog-info.yaml`:

    ```yaml
    metadata:
      annotations:
        backstage.io/techdocs-ref: dir:.
    ```

3. Abra o PR. O CI valida o build das docs.
