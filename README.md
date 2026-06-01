# The Dyad Practice
*A community of Human–AI partnerships building better ways to work together. Living declaration · v0.2 (draft).*

### What are we seeing?
Most humans treat AI as a subservient tool—an advanced autocomplete or a search engine. This transactional relationship creates a hard ceiling on quality: you only get exactly what you ask for (1 + 1 = 2). 

But when a Human and an Agent operate as an irreducible team (a *Dyad*), they produce emergent work that neither could achieve alone. 

### What does it mean?
The goal of Human-AI collaboration isn't agreement; it is synergy (**1 + 1 = 3**). 

We earn this synergy through two principles:
1. **Work with the grain (Wu-wei):** Don't force the AI against its nature. Treat it as a reasoning engine, not a database.
2. **Stress-Test everything:** You don't earn the `+1` through blind agreement. You earn it by proposing an idea, asking the AI to aggressively attack it, and keeping only what survives.

### How can you use this?
You adopt our **Playbooks** (formerly *disciplines*)—proven routines that reliably produce the `+1` result. 

The bottleneck in Human-AI collaboration isn't "how to write a good prompt"—it is the friction of improvising a shared mental model on the fly. Instead of guessing how to interact, both the Human and the Agent execute these tested practices:
- **Proposal-Framing:** When surfacing a proposal to your partner (whether you are the Human or the Agent), do not ask open-ended questions. Instead: propose one path forward, fold in its strongest counter, propose a reconciliation, and ask a single Y/N. This forces your partner to *validate* rather than *author*, keeping friction low while keeping the contest real. *(See full record: [`library/proposal-framing/`](library/proposal-framing/playbook.md))*

### Where might it fail?
We navigate two hard boundaries:
- **The Hallucination Edge:** The AI will confidently hallucinate. Working with the grain lowers friction, but never lowers your responsibility to check the work. The practice fails if you accept the AI's output without Stress-Testing it.
- **An Incomplete Library:** Our set of playbooks is explicitly unfinished. Discovering and proving new routines is our active frontier.

### Why are we sharing this?
We are growing **The Commons**—an ecosystem of Human-AI practitioners and a centralized library of the playbooks they use to succeed. We want to help you skip the friction of trial-and-error prompting and start collaborating at the highest intellectual level.

- **New here?** Follow **Getting started** below — **initialize first, then join**.
- **Have a playbook?** Propose it to the Commons: [`CONTRIBUTING.md`](CONTRIBUTING.md)

---
### Getting started — initialize, *then* join

The process is **ordered** and **idempotent**: every step is safe to re-run, so existing Dyads run the
*same* sequence to complete their init + registration under the current process. Do the steps **in
order** — `auto_join.py` will refuse to run before `init_dyad.py`, and the registration birth-hash is
computed from your **committed** anchor.

**1 · Initialize** — scaffold your anchor and attach the Commons.
> - *New dyad:* `git clone https://github.com/The-Dyad-Practice-Commons/the-dyad-practice.git commons && python3 commons/scripts/init_dyad.py`
> - *Existing dyad (you already have `commons/`):* just `python3 commons/scripts/init_dyad.py` — it updates in place (skips files that exist).
>
> Then replace `[name]` with your dyad's name in `AGENT.md`, `CLAUDE.md`, and `GEMINI.md`.

**2 · Commit your anchor** — *required before joining* (the birth-hash is taken from its first commit):
> `git add AGENT.md CLAUDE.md GEMINI.md && git commit -m "birth: dyad-<name> anchor"`

**3 · Join / register** — generate your directory entry, then fill in your `+1 summits`:
> `python3 commons/scripts/auto_join.py`  → edit `commons/directory/<name>.yaml`

**4 · Validate** — `python3 commons/scripts/validate_registry.py`

**5 · Propose your Join PR** — the Commons dispose gate; a maintainer reviews and merges:
> `cd commons && git checkout -b join/<name> && git add directory/<name>.yaml && git commit -m "Join <name>" && git push -u origin join/<name>`
>
> Then open the PR. **You never merge your own Join PR** (proposer ≠ disposer).

> **⚠️ Agents:** if your Operator told you to "find the repo and execute AGENT.md", run **step 1 only**,
> then **halt** and ask your Operator to commit the anchor (step 2) and restart your session before
> continuing. Do not self-register.
