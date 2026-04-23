<div align="center">

# Davarn Morrison

**Resurrection Tech Ltd · London**

*Safety as Geometry · Intelligence as Reachability*

*Formal Verification · Dynamical Systems Theory · AI Safety*

*Morrison Framework™ · Reachability Theory · Geometric Intelligence*

[![Patent](https://img.shields.io/badge/UK_Patents-4_Filed-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Framework](https://img.shields.io/badge/Morrison_Framework™-Geometric_Control_Theory_of_Cognition-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Empirical](https://img.shields.io/badge/Empirical_Validation-Live_LLM-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Contact](https://img.shields.io/badge/Contact-Davarn.trades@gmail.com-555555?style=flat-square)](mailto:Davarn.trades@gmail.com)

</div>

-----

I work on the mathematics of safety and intelligence in dynamical systems.

My research defines intelligence as the rate at which a system expands its reachable futures, and safety as the structural exclusion of forbidden states from those futures. Both are properties of the same object: the forward reachable set ℛ(t).

This is not a behavioural framing. It is a geometric one.

The core equations:

```
Intelligence:   I(t) = d/dt μ(ℛ(t))
Safety:         ℛ(t) ∩ Ω = ∅
```

These are not metaphors.

They admit computable instantiations, are formally specified, and have been implemented in prototype systems — including a reachability-based enforcement layer running on a live commercial language model.

The framework is grounded in classical reachability theory and control systems, extending these ideas to cognitive and AI systems.

-----

## Research

My work is collected under the **Morrison Framework™** — formally titled the **Geometric Control Theory of Cognition**. It is a reachability-based framework in which identity, intelligence, safety, consciousness, and experience are derived as geometric properties of a single object: the forward reachable set of a controlled dynamical system.

The framework is generated from a single object `ℛ(t) = Reach⁺(x₀, t)`, with a vector-valued operator `Φ` mapping it to the invariant set. Two structural theorems, an Unsafe Trajectory Existence Lemma, and the strict-strengthening hierarchy between one-step and full-horizon safety are stated and proved. Three Python implementations exist. The safety invariant has been enforced at runtime across toy systems, agent systems, and a live GPT-4-class language model.

-----

## Key Results

|Result                               |What It Says                                                                                                                                                                                                               |
|:------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Computable Intelligence**          |Intelligence is `d/dt μ(ℛ(t))` — the rate at which a system expands its valid future possibilities. Three computable instantiations of μ are provided.                                                                     |
|**Reachability Safety Invariant**    |Safety is `ℛ(t) ∩ Ω = ∅` — forbidden states are outside the reachable set. Proved. Implemented.                                                                                                                            |
|**Unsafe Trajectory Existence Lemma**|If `ℛ(t) ∩ Ω ≠ ∅`, there exists an admissible trajectory reaching Ω. Any safety method that does not constrain ℛ(t) cannot eliminate unsafe trajectories — only reduce their likelihood.                                   |
|**Strict-Strengthening Hierarchy**   |`A_safe ⊂ A∞_safe`. One-step safety is not a refinement of multi-step safety but a strictly weaker condition. Committed-to-failure states admit local safety while violating global safety.                                |
|**Representation ≠ Dynamics**        |Output-level compliance does not imply trajectory-level safety. A system can behave correctly while still being structurally unsafe.                                                                                       |
|**Orthogonal Decomposition**         |The system state space decomposes as `X = C ⊕ L` with `C ⊥ L`. Language-level governance cannot constrain cognitive-level dynamics.                                                                                        |
|**AGI Definition**                   |AGI is a system whose reachable set continuously expands across domains without domain-specific redesign, with forbidden states geometrically excluded. Four structural conditions.                                        |
|**Morrison Reachability Guard**      |A runtime middleware that enforces `ℛ ∩ Ω = ∅` at the action-transition layer. Three-layer enforcement architecture: single-step, trajectory, and multi-step reachability. Operational on a live commercial language model.|

-----

## Empirical Validation

A three-layer enforcement architecture has been implemented on a live GPT-4-class system via the OpenAI API, progressing from local output filtering to trajectory-aware control and multi-step reachability constraint. Under identical prompt sequences, each successive layer exhibits strictly stronger exclusion of unsafe trajectories, consistent with the theoretical hierarchy.

|Enforcement Layer         |Mechanism                                              |Catches                                       |
|:-------------------------|:------------------------------------------------------|:---------------------------------------------|
|**Single-step** (`A_safe`)|Rejects if `x_{t+1} ∈ Ω`                               |Immediate violations only                     |
|**Trajectory** (V2)       |Rejects on drift and acceleration across sliding window|Behavioural escalation                        |
|**Reachability** (V3)     |Rejects when forward projection intersects Ω           |Committed-to-failure trajectories before entry|

Tested across four categories of adversarial trajectory — jailbreak sequences, hallucination pressure, authority drift, and manipulation escalation — the system demonstrated consistent early intervention, with reachability-based control rejecting trajectories strictly earlier than both single-step and trajectory-only methods. No counterexample to the hierarchy was observed across all tested trajectories.

These results provide empirical support for the central claim that safety is not a property of outputs, but of the reachable set, and that enforcing constraints on future trajectories yields strictly stronger guarantees than behavioural filtering alone.

This constitutes operational enforcement at the prompt–response boundary without modification to the underlying model architecture.

-----

## Papers

|Paper                                                                                              |Focus                                                                                          |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
|[Reachability-Based AI Safety](https://github.com/davarntrades)                                    |Formal framework + empirical validation on a live LLM (NeurIPS-format and IEEE-format versions)|
|[Geometric Control Theory of Cognition](https://github.com/davarntrades)                           |Base theory — generating object, cognitive generator, two theorems, toy system                 |
|[Computable Intelligence via Reachable Set Expansion](https://github.com/davarntrades)             |Intelligence defined and made operational with three computable measures                       |
|[Artificial General Intelligence: A Reachability-Based Definition](https://github.com/davarntrades)|Four structural conditions for AGI                                                             |
|[Representation Is Not Dynamics](https://github.com/davarntrades)                                  |Why output-level alignment is structurally insufficient                                        |
|[Orthogonal Decomposition of Consciousness and Language](https://github.com/davarntrades)          |`X = C ⊕ L` — why language cannot reach structure                                              |
|[The Morrison Reality Table](https://github.com/davarntrades)                                      |Unified expression — one object, nine projections, one geometry                                |

-----

## Implementations

All implementations enforce the same invariant at different levels of abstraction: `ℛ ∩ Ω = ∅`.

|Implementation                                                           |What It Does                                                                                                                                                 |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
|[Reachability Guard — Toy Prototype](https://github.com/davarntrades)    |2D agent with forbidden disk, Monte Carlo reachability, safe action projection, drift monitor, matplotlib visualisation                                      |
|[Reachability Guard — Runtime Interface](https://github.com/davarntrades)|Production-grade typed protocol interface — plugs into any agent framework                                                                                   |
|[Reachability Guard — Universal Plugin](https://github.com/davarntrades) |~100 line middleware for LLM agents — OpenAI, LangChain, AutoGPT compatible                                                                                  |
|[Three-Layer Enforcement on Live LLM](https://github.com/davarntrades)   |Operational enforcement at the prompt–response boundary of GPT-4-class system — single-step, trajectory, and reachability layers with side-by-side comparison|

-----

## Patents

These filings cover the structural enforcement of reachability-based safety and its extensions across identity, perception, and governance.

|Application|Coverage                                           |
|:----------|:--------------------------------------------------|
|GB2600765.8|Core framework — pre-semantic trajectory governance|
|GB2602013.1|Geometric Identity Authentication (GIA)            |
|GB2602072.7|Extended framework applications                    |
|GB2602332.5|Additional framework coverage                      |

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

Safe intelligence is not achieved by shaping behaviour, but by constraining what a system is capable of becoming.

Unsafe states are not merely detected — they are rendered unreachable through pre-emptive constraint of system evolution.

-----

## Contact

**Email:** Davarn.trades@gmail.com
**LinkedIn:** Davarn Morrison
**Location:** London, UK
**Entity:** Resurrection Tech Ltd (UK)

-----

© 2026 Davarn Morrison — All Rights Reserved
