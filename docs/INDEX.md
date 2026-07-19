# 📚 Índice Central de Documentação — onion-standalone

> **Gerado por**: adoção role-scoped (`/meta:adopt`) | **Contagens**: derivadas de [`docs/onion/inventory.md`](onion/inventory.md) (SSOT rescaneada do filesystem)

Hub de navegação da documentação deste repositório.

---

## 🎯 Visão Geral

Este é o **onion-standalone** — a **porta pública Claude** do Sistema Onion: uma instância
**adotada role-scoped** (bundle `standalone`) do framework `.claude/`. Cobre o ciclo de
desenvolvimento com Claude Code nas dimensões **produto**, **engenharia**, **testes** e **documentação**.

- 🤖 **75 comandos invocáveis** em 7 categorias + root (`git`, `engineer`, `product`, `test`, `validate`, `docs`, `meta`*)
- 🎯 **37 agentes de IA especializados** em 7 categorias (development, product, git, testing, review, deployment, meta)
- 🧩 **7 skills** em `.claude/skills/` (`onion`, `onion-patterns`, `onion-validation`, `onion-orchestration`, `language-standards`, `onion-engineering-context`, `onion-product-context`)
- 📚 **78 Knowledge Bases** de framework (conceitos, frameworks, padrões, agentic-patterns)
- 🔗 **Task Manager Abstraction** plugável (Jira, ClickUp, Asana, Linear) + **Forge Abstraction** (GitHub)
- 🏗️ **Spec as Code** — business, technical context (templates a popular no projeto)

> **Porta ≠ core.** Este repo é uma **derivação que cita** o core privado `onion-evolve` — leva o
> recorte operacional do bundle `standalone`. Inclui as **ferramentas de trabalho** meta (`*` — kg,
> diary, orchestrate, metaspec-validate, constellation, co-evolução upstream…), mas **sem** a
> **meta-fábrica** (`create-*`/`adopt`/`federation-*`/`evolve`/`graph`/`inventory` — autoria e
> federação ficam no core), sem a memória privada de evolução e sem os `.kg.yaml` do core (você gera
> os **seus**). Ver [`public-door-vs-private-core`](knowledge-base/concepts/public-door-vs-private-core.md).

---

## 🗂️ Estrutura

| Área | Caminho | Conteúdo |
|------|---------|----------|
| **Inventário canônico** | [`docs/onion/inventory.md`](onion/inventory.md) | SSOT de contagens (gerada do filesystem) |
| **Meta-specs (L0)** | [`docs/meta-specs/`](meta-specs/) | Constituição do framework (arquitetura, comandos, agentes, code-standards, integrações) |
| **Knowledge Bases** | [`docs/knowledge-base/`](knowledge-base/index.md) | Conceitos, frameworks, padrões, agentic-patterns |
| **SDAAL** | [`docs/sdaal/`](sdaal/) | Padrão Specification-Driven AI Abstraction Layer |
| **Business context** | `docs/business-context/` | Contexto de negócio (template — popular no projeto) |
| **Technical context** | `docs/technical-context/` | Contexto técnico (template — popular no projeto) |

---

## 🚀 Por onde começar

1. `/warm-up` — carrega o contexto do projeto.
2. `/onion` — ponto de entrada inteligente (recomenda comando/agente/fluxo).
3. `/engineer:help` — o ciclo de engenharia faseado (plan → start → work → pre-pr → pr).
4. `/docs:build-tech-docs` — gerar o contexto técnico do projeto.
