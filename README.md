# aj's market

Marketplace de plugins do Claude Code do **alexpatri**.

> Identificador do marketplace: `ajs-market` (é o que vai depois do `@` ao
> instalar). "aj's market" é só o nome de exibição — o campo `name` do
> `marketplace.json` precisa ser kebab-case.

## Como usar

No Claude Code:

```
/plugin marketplace add alexpatri/marketplace
/plugin install <plugin>@ajs-market
```

## Plugins

| Plugin | Descrição | Fonte |
| --- | --- | --- |
| **kolb** | Modo aprendizado para Claude Code — ciclo de Kolb, bloqueio de geração e tutor isolado. | [`alexpatri/kolb`](https://github.com/alexpatri/kolb) · `plugin/kolb` (`git-subdir`) |

Cada plugin é referenciado a partir do seu próprio repositório (via `source`),
então tem ciclo de vida independente deste marketplace.

## Adicionar um plugin

Acrescente uma entrada em `plugins` no `.claude-plugin/marketplace.json`. A
`source` pode ser:

- **outro repo GitHub** — `{"source": "github", "repo": "owner/repo"}`
- **subdiretório de um repo** — `{"source": "git-subdir", "url": "owner/repo", "path": "sub/dir"}`
- **local (neste repo)** — `"./plugins/meu-plugin"`
- **URL git genérica** — `{"source": "url", "url": "https://…git"}`
- **npm** — `{"source": "npm", "package": "@scope/pkg"}`

Todas aceitam `ref` (branch/tag) e `sha` (commit) opcionais para fixar versão.
