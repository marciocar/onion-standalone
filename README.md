# 🧅 Onion — a maquinaria

> **Este repositório é uma PROJEÇÃO, não a fonte.** Ele é materializado do core por
> `ops/materialize-door.sh` e **não recebe PR** — uma correção feita aqui é sobrescrita na próxima
> materialização. O caminho de contribuição é o canal de sinais descrito em `docs/evolution/`.

O Onion é um framework de método executável para Claude Code: comandos invocáveis, agentes
especializados, skills e — o que o distingue — **guardas determinísticas** que reprovam em CI. Ele
cobre três dimensões peer do ciclo: produto, engenharia e compliance.

## O que está aqui, e o que não está

**Está:** a maquinaria completa — `.claude/` (comandos, agentes, skills, hooks, utils, validation),
as meta-specs e a knowledge base.

**Não está, e é desenho:** a **biografia** do core — diário, análises, discussões, registro da
federação e materiais. Método viaja; história, não. A allowlist que decide isso é
`.claude/utils/adopt/vendor-manifest.sh`, e ela falha FECHADA: o que não está declarado não viaja.

## Como usar

```bash
git clone https://github.com/marciocar/onion-standalone.git
cd onion-standalone && claude
```

Depois, `/warm-up` para o contexto e `/onion` para a orientação. As guardas rodam com
`bash .claude/validation/lint-artifacts.sh`.

## Licenças

**Código** (`.claude/**`, scripts): MIT — `LICENSE`.
**Documentação e doutrina** (`docs/**`): CC BY-NC 4.0 — `LICENSE-DOCS`.

---

Materializado do core no pin `685140eadd7d` · papel `standalone`.
