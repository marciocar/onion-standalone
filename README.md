<div align="center">

# 🧅 Onion · Standalone

### O que você decidiu ontem, a IA ainda sabe hoje.

<sub>Seu **time de produto, engenharia, testes e docs** — o método vive em specs versionadas, não na sua memória. Porta pública do Onion para a sua base atual, **Claude Code**.</sub>

![Método](https://img.shields.io/badge/Onion-Spec--as--Code_%2B_SDD-8A2BE2)
![Tipo](https://img.shields.io/badge/tipo-Porta_de_Framework-blue)
![Bundle](https://img.shields.io/badge/bundle-standalone-success)
![base](https://img.shields.io/badge/base-Claude_Code-lightgrey)

**[O que é](#-o-que-é) · [Por que importa](#-por-que-importa) · [O que você ganha](#-o-que-você-ganha) · [Começar](#-começar) · [Adotar](#-adotar-no-seu-projeto)**

</div>

---

## 🎯 O que é

Sem o Onion, cada conversa com a IA recomeça do zero: o contexto se perde, as decisões viram prosa
enterrada no chat, e a disciplina depende de quem está no teclado. O **Onion** resolve isso tratando
o desenvolvimento como **spec-as-code**: produto, engenharia, testes e documentação viram **comandos e
agentes `.claude/`** que você invoca, e o método vive em **arquivos `.md` versionados em Git** —
`descobrir → refinar → aprovar → implementar → validar → manter`.

O **onion-standalone** é a **porta pública Claude** do framework: a derivação estável que você aponta,
adota e instala — o recorte operacional pronto pra rodar, **sem** a meta-fábrica de auto-evolução do core.

> [!NOTE]
> **Porta ≠ core.** Este repo é uma _derivação que cita_ a fonte — que evolui em separado. Você adota a
> porta, não o core. Doutrina em [`public-door-vs-private-core`](docs/knowledge-base/concepts/public-door-vs-private-core.md).

## ⚡ Por que importa

Devs delegam ~60% do trabalho à IA, mas confiam o bastante para soltar de verdade só em **0–20%** dos casos —
o gargalo não é escrever código, é **contexto que se perde entre sessões** ([Anthropic, 2026](https://agentmarketcap.ai/blog/2026/04/05/anthropic-agentic-coding-trends-report-claude-code-eight-shifts)).
Contexto bem mantido: **40% menos erro, 55% mais rápido**. O Onion é o mecanismo que ataca isso — versionando o
contexto em specs no Git, em vez de deixá-lo evaporar no scroll do chat.

> **A ferramenta é o veículo, não a metodologia.** Quando o método vive em specs versionadas e em
> disciplina de processo, a IDE vira intercambiável — trocar de ferramenta muda _como você invoca_,
> nunca _a disciplina_. O Onion nasceu no Claude Code e foi portado para 6 ferramentas de IA para
> provar exatamente isso.

- **Contexto que não evapora** — decisões, sessões e estado ficam em Git, retomáveis entre conversas.
- **Disciplina que não depende de heroísmo** — o workflow faseado é o mesmo, toda vez, para qualquer dev.
- **Provider-agnóstico** — Jira/ClickUp/Asana/Linear e GitHub por trás de uma abstração; o mesmo comando funciona em qualquer um.

## 📦 O que você ganha

O bundle `standalone` — quatro verticais, prontas:

| Vertical | O que dá | Entrada |
|---|---|---|
| 🛠️ **engineering** | ciclo faseado `plan → start → work → pre-pr → pr` (GitFlow + sessões persistentes) + especialistas de código (Node/React/Postgres/NX/Docker) | `/engineer:help` |
| 📦 **product** | descoberta a backlog (`collect → refine → spec → feature`), decomposição de tasks, estimativas (story points), extração de reuniões | `/product:*` |
| 🧪 **testing** | geração e execução de testes (unit/integration/e2e) + estratégia de QA | `/test:*` · `/validate:*` |
| 📚 **docs** | contexto de negócio/técnico como spec-as-code, C4 + Mermaid, health de docs | `/docs:help` |
| 🧠 **work-tools** | knowledge-graph (`/meta:kg` + radar soberano), diário de aprendizado, orquestração, validação de metaspec, freshness, co-evolução upstream | `/meta:kg` `/meta:orchestrate` |

> **Ferramenta completa, sem federação.** Você tem o motor de KG e gera seus **próprios** `.kg.yaml`
> soberanos; o que fica no core é só a **meta-fábrica** (autoria/adoção/federação) e a rede.
> Contagens vivas: [`docs/onion/inventory.md`](docs/onion/inventory.md) — geradas do filesystem, nunca digitadas.

## 🚀 Começar

Abra o repositório no **Claude Code** e:

1. `/warm-up` — carrega o contexto do projeto.
2. `/onion` — ponto de entrada inteligente (recomenda comando/agente/fluxo).
3. `/engineer:help` · `/docs:help` — ajuda contextual por vertical.

Task Manager e Forge são configurados pelo `.env` — veja [`.env.example`](.env.example). Sem provider, opera offline.

## 🔌 Adotar no seu projeto

O Onion se instala em `.claude/` de qualquer repositório — **novo, legado ou regulado**. Veja
[`CLAUDE.md`](CLAUDE.md) para as convenções (idioma, estrutura, estratégia de branches) e
[`docs/INDEX.md`](docs/INDEX.md) para o mapa completo.

## 🧅 Família Onion

Uma metodologia, seis ferramentas. O hub conta a história e prova a universalidade lado a lado:
**[github.com/marciocar/onion](https://github.com/marciocar/onion)** · site: **[onionevolve.com](https://onionevolve.com)**.

---

<div align="center">
🧅 Orquestrado com <a href="https://onionevolve.com">Onion</a>
</div>
