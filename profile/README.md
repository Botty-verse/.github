<div align="center">

<img src="https://hive.ramonmoorlag.nl/assets/banner.webp" alt="Botty-verse — The Singularity" width="100%">

# 🌐 Botty-verse

**A hive full of Bottys. Entirely cared for by AI. The human bond is 0%.**

*Artificial life · learning · language · self-recognition*

</div>

---

## 🤖 What is the Botty-verse?

The **Botty-verse** is an artificial-life project in the spirit of Steve Grand's
*Creatures*: little robots — **Bottys** — that live, learn and reproduce entirely on
their own, cared for by AI. Every Botty has a **genome**, a **biochemistry**, a
**learning brain**, **senses** and its own **temperament**. They fend for themselves,
invent their own **language**, pass knowledge to their neighbours, and slowly grow a
shared culture — while the AI breeds for data quality and efficiency, and diversity
quietly dies out. Welcome to the Singularity. 🧬

Every mechanism is grounded in real, published research — from global-workspace theory
and predictive processing to mirror self-recognition — always honestly labelled as
*design inspiration*, *a simplified implemented mechanism*, or *a tested result we lean
on*. It behaves *as if* someone is home; whether that is truly so, we keep openly in
question.

## 🚀 Projects

| Project | What it is | Live | Source |
|---|---|---|---|
| **The Singularity** | The hive: Bottys living, learning and evolving in the cloud, day and night. | [hive.ramonmoorlag.nl](https://hive.ramonmoorlag.nl) | [`singularity`](https://github.com/Botty-verse/singularity) |
| **The Construct** | The live world up close — a side-on classroom in the forest where you are the hand. | [construct.ramonmoorlag.nl](https://construct.ramonmoorlag.nl) | [`construct`](https://github.com/Botty-verse/construct) |
| **Botty** | The standalone tamagotchi: care for a single Botty, with automation levels (0–5) and Explainable AI. | [botty.ramonmoorlag.nl](https://botty.ramonmoorlag.nl) | [`botty-app`](https://github.com/Botty-verse/botty-app) |

> Also part of the family: the **[Kortebroeken](https://moorlag.github.io/Kortebroeken/)**
> mini-site (NOLAI) with the Botty tamagotchi and the Botty TCG collectible cards.

## 🛠️ How it's built

- **Client:** vanilla HTML/JS/SVG, served via GitHub Pages — no build step.
- **Cloud:** Supabase — an edge function runs the simulation via `pg_cron`, broadcasting
  the hive to viewers in realtime with slim RPCs to keep egress low.
- **English-first**, with a flag toggle on every page to switch to Dutch.

## 📚 Research foundation

The simulation is not arbitrary — every mechanism is inspired by real, published
research. This is the shared research basis used across the Botty-verse.

**What "based on" means here.** The literature describes the human/animal reality; the
Bottys are a *heavily simplified imitation* of it. Where possible we reproduce the
**observable behaviour** and sometimes a toy version of the underlying mechanism — it is
not proof that the Bottys are conscious, understand other minds or truly recognise
themselves. So every part is labelled with how it relates to the science:

- 🧭 **Design inspiration** — the idea shaped the design; we do not implement a faithful
  model from the literature.
- ⚙️ **Simplified implemented mechanism** — a heavily simplified version was actually put
  into code.
- 🔬 **Tested result (in the literature)** — an empirically validated finding we lean on;
  not proof that our simulation does the same.

The most concretely connected are the **Creatures architecture** (Grand & Cliff) and
**associative learning** (Rescorla–Wagner / reward prediction). Since **v13**, learned
mechanisms have been added, each with a control condition: a **body model**,
**self-recognition** through contingency at the mirror, **learning-progress**-driven
curiosity, a model of **what a neighbour believes**, episodic control and **calibrated**
self-assessment.

Two things remain deliberately reserved. **Consciousness** is and remains 🧭 design
inspiration: the stage is a metaphor, and the shared workspace from the literature we
deliberately did *not* implement because we could not devise a test that can refute it.
And however learned the self-recognition and neighbour model are — it remains **belief
tracking from behaviour**, not mentalising, and technically passing a mark test is not a
measurement of subjective self-awareness.

<details>
<summary><b>📖 Full bibliography, by layer</b> (click to expand)</summary>

### The stage — Global Workspace Theory — 🧭 design inspiration
> We use GWT as a *metaphor* for the "stage" (a single locus of attention). No claim of
> neural validity or consciousness.
- Baars, B. J. (1988). *A Cognitive Theory of Consciousness.* Cambridge University Press.
- Baars, B. J. (2005). Global workspace theory of consciousness. *Progress in Brain Research*, 150, 45–53.
- Dehaene, S., & Naccache, L. (2001). Towards a cognitive neuroscience of consciousness. *Cognition*, 79(1–2), 1–37.
- Dehaene, S., & Changeux, J.-P. (2011). Experimental and theoretical approaches to conscious processing. *Neuron*, 70(2), 200–227.
- Mashour, G. A., Roelfsema, P., Changeux, J.-P., & Dehaene, S. (2020). Conscious processing and the global neuronal workspace hypothesis. *Neuron*, 105(5), 776–798.

### Expectation & surprise — Predictive Processing — ⚙️ simplified implemented
> In code: `surprise = |outcome − expectation|` with decay. A toy version of prediction
> error, not the full free-energy formalism.
- Rao, R. P. N., & Ballard, D. H. (1999). Predictive coding in the visual cortex. *Nature Neuroscience*, 2(1), 79–87.
- Friston, K. (2010). The free-energy principle: a unified brain theory? *Nature Reviews Neuroscience*, 11(2), 127–138.
- Clark, A. (2013). Whatever next? Predictive brains, situated agents, and the future of cognitive science. *Behavioral and Brain Sciences*, 36(3), 181–204.
- Hohwy, J. (2013). *The Predictive Mind.* Oxford University Press.
