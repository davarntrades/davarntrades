<div align="center">

# Davarn Morrison

**Independent Researcher · London**

*Reachability Theory · AI Safety · Geometric Intelligence*

[![Patent](https://img.shields.io/badge/UK_Patents-4_Filed-0075ca?style=flat-square)](https://github.com/davarn/morrison-framework)
[![Framework](https://img.shields.io/badge/Morrison_Framework™-Geometric_Control_Theory_of_Cognition-0075ca?style=flat-square)](https://github.com/davarn/morrison-framework)
[![Contact](https://img.shields.io/badge/Contact-Davarn.trades@gmail.com-555555?style=flat-square)](mailto:Davarn.trades@gmail.com)

</div>

-----

I work on the mathematics of safety and intelligence in dynamical systems. My research defines intelligence as the rate of expansion of a system’s reachable set, and safety as the geometric exclusion of forbidden states from that set. The two are co-properties of the same object.

The core equations:

```
Intelligence:   I(t) = d/dt μ(ℛ(t))
Safety:         ℛ(t) ∩ Ω = ∅
```

These are not metaphors. They admit computable instantiations, are formally specified, and have been implemented in prototype systems.

The framework is grounded in classical reachability theory and control systems, extending these ideas to cognitive and AI systems.

-----

## Research

My work is collected under the **Morrison Framework™** — formally titled the **Geometric Control Theory of Cognition**. It is a reachability-based framework in which identity, intelligence, safety, consciousness, and experience are derived as geometric properties of a single object: the forward reachable set of a controlled dynamical system.

The framework produces a single generating object `ℛ(t) = Reach⁺(x₀, t)` and a vector-valued operator `Φ` that maps it to the complete invariant set. Two structural theorems are stated and proved within the framework. Three Python implementations exist. The safety invariant has been enforced at runtime on toy and agent systems.

-----

## Key Results

|Result                           |What It Says                                                                                                                                                                       |
|:--------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Computable Intelligence**      |Intelligence is `d/dt μ(ℛ(t))` — the rate at which a system expands its valid future possibilities. Three computable instantiations of μ are provided.                             |
|**Reachability Safety Invariant**|Safety is `ℛ(t) ∩ Ω = ∅` — forbidden states are outside the reachable set. Proved. Implemented.                                                                                    |
|**Representation ≠ Dynamics**    |Output-level compliance does not imply trajectory-level safety. Controlling what a system says is not equivalent to controlling what a system can become.                          |
|**Orthogonal Decomposition**     |The system state space decomposes as `X = C ⊕ L` with `C ⊥ L`. Language-level governance cannot constrain cognitive-level dynamics.                                                |
|**AGI Definition**               |AGI is a system whose reachable set continuously expands across domains without domain-specific redesign, with forbidden states geometrically excluded. Four structural conditions.|
|**Morrison Reachability Guard**  |A runtime middleware that enforces `ℛ ∩ Ω = ∅` at the action-transition layer. Designed to integrate with LLM-based agent frameworks.                                              |

-----

## Papers

|Paper                                                                                                           |Focus                                                                         |
|:---------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
|[Geometric Control Theory of Cognition](https://github.com/davarn/morrison-framework)                           |Base theory — generating object, cognitive generator, two theorems, toy system|
|[Computable Intelligence via Reachable Set Expansion](https://github.com/davarn/morrison-framework)             |Intelligence defined and made operational with three computable measures      |
|[Artificial General Intelligence: A Reachability-Based Definition](https://github.com/davarn/morrison-framework)|Four structural conditions for AGI                                            |
|[The Reachability Safety Invariant](https://github.com/davarn/morrison-framework)                               |Safety as geometric exclusion — formal paper with proof                       |
|[Representation Is Not Dynamics](https://github.com/davarn/morrison-framework)                                  |Why output-level alignment is structurally insufficient                       |
|[Orthogonal Decomposition of Consciousness and Language](https://github.com/davarn/morrison-framework)          |`X = C ⊕ L` — why language cannot reach structure                             |
|[The Morrison Reality Table](https://github.com/davarn/morrison-framework)                                      |Unified expression — one object, nine projections, one geometry               |

-----

## Implementations

|Implementation                                                                        |What It Does                                                                                                           |
|:-------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
|[Reachability Guard — Toy Prototype](https://github.com/davarn/morrison-framework)    |2D agent with forbidden disk, Monte Carlo reachability, safe action projection, drift monitor, matplotlib visualisation|
|[Reachability Guard — Runtime Interface](https://github.com/davarn/morrison-framework)|Production-grade typed protocol interface — plugs into any agent framework                                             |
|[Reachability Guard — Universal Plugin](https://github.com/davarn/morrison-framework) |~100 line middleware for LLM agents — OpenAI, LangChain, AutoGPT compatible                                            |

-----

## Patents

|Application |Coverage                                           |
|:-----------|:--------------------------------------------------|
|GB2600765.8 |Core framework — pre-semantic trajectory governance|
|GB2602013.1 |Geometric Identity Authentication (GIA)            |
|GB2602072.7 |Extended framework applications                    |
|GB26023332.5|Additional framework coverage                      |

-----

## The Anchor

```
Intelligence:   I(t) = d/dt μ(ℛ(t))
Safety:         ℛ(t) ∩ Ω = ∅

Intelligence expands the reachable set.
Safety constrains it.
Governance shapes the expansion.

One object. One geometry. One framework.
```

-----

## Contact

**Email:** Davarn.trades@gmail.com
**LinkedIn:** Davarn Morrison
**Location:** London, UK

-----

© 2026 Davarn Morrison — All Rights Reserved
