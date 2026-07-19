# 🧅 onion-standalone — Claude Code Rules

## 🎯 Identidade

Este é o **onion-standalone** — a **porta pública Claude** do Sistema Onion. É uma instância
**adotada role-scoped** (bundle `standalone`) do framework `.claude/`, provendo o ciclo de
desenvolvimento com Claude Code nas dimensões **produto**, **engenharia**, **testes** e **documentação**.

- **Porta ≠ core.** Este repositório é uma **derivação que cita** o core privado `onion-evolve`.
  Leva o recorte operacional do bundle `standalone` — **sem** a meta-factory (comandos `/meta:*` de
  autoria, adoção, federação, evolução, grafo), **sem** a memória privada de evolução, **sem** os
  knowledge graphs. Proveniência do core em `.claude/.onion-version` (`source_commit`).
- **Superfície instalada** (SSOT — nunca digite à mão, rode `bash .claude/validation/inventory.sh --markdown`):
  ver [`docs/onion/inventory.md`](docs/onion/inventory.md). Categorias de comando: `git`, `engineer`,
  `product`, `test`, `validate`, `docs`, `meta` (ferramentas de trabalho: kg/diary/orchestrate/…, **sem**
  a meta-fábrica de autoria/federação).
- **Atualização**: o core sincroniza este repo via `/meta:adopt --update` (vendor-branch 3-way).

## 🔌 Task Manager — Detecção e Roteamento

Provider-agnóstico via SDAAL (`.claude/utils/task-manager/`). **Antes de operar com tasks**, carregue o
`.env` e leia `TASK_MANAGER_PROVIDER` (`jira` | `clickup` | `asana` | `linear` | `none`) +
`TASK_MANAGER_TRANSPORT` (`api` default | `mcp`). Delegue ao especialista do provider ativo
(`@jira-specialist`, `@clickup-specialist`) ou ao `@task-specialist` (agnóstico). Fallback gracioso:
variável ausente → avisar em pt-BR + sugerir reconfiguração; nunca inventar valores.

## 🐙 Forge — Operações de Host Remoto (PR, review, CI)

Abstraído via SDAAL (`.claude/utils/forge/`). Comandos `/git/*` e `/engineer:pr` **nunca** chamam
`gh`/API direto — passam pelo adapter. `FORGE_PROVIDER` (default: detecta pelo remote `origin`) e
`FORGE_TRANSPORT` (`cli` default | `api`). Git local (branch/merge/tag/push) é `git` direto.

## 📝 Diretrizes de Linguagem

Autoridade canônica: skill **`language-standards`**.
- **Chat, comentários, docs, READMEs, mensagens ao usuário**: Português brasileiro (pt-BR)
- **Código, variáveis, funções, nomes de arquivo/branch, commits, logs**: Inglês (Conventional Commits)

## 🛠️ Padrões Técnicos

- Comandos: `.claude/commands/` por categoria · Agentes: `.claude/agents/<categoria>/` (YAML header + Markdown)
- Sessões de desenvolvimento: `.claude/sessions/<feature>/`
- **Spec as Code**: Business (`docs/business-context/`), Technical (`docs/technical-context/`),
  Knowledge Bases (`docs/knowledge-base/`), Meta-specs L0 (`docs/meta-specs/`)
- **Estratégia de branches**: produto na branch principal do projeto; a evolução do framework Onion
  chega pela branch de integração (ver `.claude/.onion-version`). GitFlow via `@gitflow-specialist`.

## 🚀 Entrada

- `/warm-up` — carrega o contexto do projeto
- `/onion` — ponto de entrada inteligente (recomenda comando/agente/fluxo)
- `/engineer:help` · `/docs:help` — ajuda contextual por vertical
