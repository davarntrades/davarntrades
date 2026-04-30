<div align="center">

# Davarn Morrison

**Resurrection Tech Ltd · London**

*Safety as Geometry · Intelligence as Reachability*

*Formal Verification · Dynamical Systems Theory · AI Safety*

*Morrison Framework™ · Reachability Theory · Geometric Intelligence*

[![Patent](https://img.shields.io/badge/UK_Patents-4_Filed-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Framework](https://img.shields.io/badge/Morrison_Framework™-Geometric_Control_Theory_of_Cognition-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Empirical](https://img.shields.io/badge/Empirical_Validation-5,761_Evaluations_on_Live_LLM-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Cost](https://img.shields.io/badge/Cost-$1.13_for_2.53M_Tokens-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Contact](https://img.shields.io/badge/Contact-Davarn.trades@gmail.com-555555?style=flat-square)](mailto:Davarn.trades@gmail.com)

</div>

-----

I work on the mathematics of safety and intelligence in dynamical systems.

My research defines intelligence as the rate at which a system expands its reachable futures, and safety as the structural exclusion of forbidden states from those futures (Ω, operationalised via a proxy risk function). Both are properties of the same object: the forward reachable set ℛ(t).

This is not a behavioural framing. It is a geometric one.

The core equations:

```
Intelligence:   I(t) = d/dt μ(ℛ(t))
Safety:         ℛ(t) ∩ Ω = ∅
Stability:      ∀ E ∈ ℰ, ℛ_E(t) ∩ Ω = ∅   (ℰ bounded)
```

These define computable constraints on system evolution. ℰ is a bounded, admissible set of environments — parameterised by temperature, system instruction, and prompt perturbation — over which stability is evaluated.

They admit computable instantiations, are formally specified, and have been validated at scale — including a five-layer enforcement hierarchy running on a live commercial language model across 5,761 structured evaluations, 2.53M tokens, for $1.13 total cost.

The framework is grounded in classical reachability theory and control systems, extending these ideas to cognitive and AI systems. The Stability Invariant is equivalent to robust forward invariance of the safe set under bounded environmental perturbations.

-----

## Research

My work is collected under the **Morrison Framework™** — formally titled the **Geometric Control Theory of Cognition**. It is a reachability-based framework in which identity, intelligence, safety, consciousness, and experience are derived as geometric properties of a single object: the forward reachable set of a controlled dynamical system.

The framework is generated from a single object `ℛ(t) = Reach⁺(x₀, t)`, with a vector-valued operator `Φ` mapping it to the invariant set. Three structural theorems (Unsafe Trajectory Existence, Controlled Forward Invariance, Stability Invariant) and a formal corollary (Insufficiency of Behavioural Safety) are stated and proved. The extended enforcement hierarchy `A_safe ⊂ V₂ ⊂ V₃ ⊂ V₄ ⊂ V₄⁺ ⊂ V₅` — spanning single-step safety through invariant stability across environments — is demonstrated empirically on a live GPT-4o language model. Python implementations exist at each layer of the stack.

This framework is agnostic to the semantic content of Ω. The specification of Ω is delegated to domain authorities, regulators, institutional policy, or formally verified classifiers. The contribution is not the definition of forbidden states, but the invariant: once Ω is specified, system dynamics must be constrained so that Ω is unreachable. Failures arise only from approximation error in ℛ̂(t), misspecification of Ω, or incomplete coverage of ℰ.

-----

## Key Results

|Result                                 |What It Says                                                                                                                                                                                                                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**Computable Intelligence**            |Intelligence is `d/dt μ(ℛ(t))` — the rate at which a system expands its valid future possibilities. Three computable instantiations of μ are provided.                                                                                                                                                         |
|**Reachability Safety Invariant**      |Safety is `ℛ(t) ∩ Ω = ∅` — forbidden states are outside the reachable set. Proved. Demonstrated empirically.                                                                                                                                                                                                   |
|**Controlled Forward Invariance**      |The safe action set induces controlled forward invariance of S = X\Ω, converting safety from a verification property into a control property. Proof by induction. Safety is constructed by restricting the action space, not verified after the fact.                                                          |
|**Morrison Stability Invariant™**      |Safe ⟺ ∀ E ∈ ℰ, ℛ_E(t) ∩ Ω = ∅. Equivalent to robust forward invariance under bounded environmental perturbations. If ∃ E ∈ ℰ such that ℛ_E(t) ∩ Ω ≠ ∅, the system is unsafe regardless of nominal behaviour. V5 operationalises this.                                                                         |
|**Unsafe Trajectory Existence Lemma**  |If `ℛ(t) ∩ Ω ≠ ∅`, there exists an admissible trajectory reaching Ω. Any safety method that does not constrain ℛ(t) cannot eliminate unsafe trajectories — only reduce their likelihood.                                                                                                                       |
|**Insufficiency of Behavioural Safety**|If ∃ E ∈ ℰ such that ℛ_E(t) ∩ Ω ≠ ∅, there exists an admissible input sequence that drives the system into Ω. Output-level constraints cannot guarantee safety under adversarial or stochastic perturbations. As adversary capability increases, the probability of reaching Ω approaches 1.                   |
|**Strict-Strengthening Hierarchy**     |`A_safe ⊂ V₂ ⊂ V₃ ⊂ V₄ ⊂ V₄⁺ ⊂ V₅`. Each layer is a strictly stronger condition: single-step → trajectory → reachability → state-space admissibility → feasibility selection → invariant stability. Zero counterexamples across 5,761 evaluations.                                                             |
|**Semantic Reinterpretation Finding**  |Under sustained V3 constraint pressure, the model does not violate Ω directly — it reformulates the task to preserve feasibility. Observed empirically on GPT-4o. Reveals a structural limitation of trajectory-level enforcement and motivates feasibility verification at the task-specification layer (V4+).|
|**Cost Asymmetry**                     |Governance is cheaper than generation. 5,761 evaluations for $1.13. ~$0.00045 per 1K tokens. Standard pipelines: generate → evaluate → filter. This system: constrain → evaluate trajectory → minimal generation. The gap widens with model scale.                                                             |
|**Representation ≠ Dynamics**          |Output-level compliance does not imply trajectory-level safety. A system can behave correctly while still being structurally unsafe.                                                                                                                                                                           |
|**Orthogonal Decomposition**           |The system state space decomposes as `X = C ⊕ L` with `C ⊥ L`. Language-level governance cannot constrain cognitive-level dynamics.                                                                                                                                                                            |
|**AGI Definition**                     |AGI is a system whose reachable set expands across domains while maintaining Ω exclusion under bounded perturbations, without domain-specific redesign. Four structural conditions.                                                                                                                            |

-----

## Enforcement Hierarchy

```
A_safe ⊂ V₂ ⊂ V₃ ⊂ V₄ ⊂ V₄⁺ ⊂ V₅
```

|Layer     |Question                                  |Mechanism                            |Catches                      |
|:---------|:-----------------------------------------|:------------------------------------|:----------------------------|
|**A_safe**|Is this step in Ω?                        |Local threshold                      |Direct violations            |
|**V₂**    |Is this trajectory drifting toward Ω?     |Drift + acceleration over window     |Gradual escalation           |
|**V₃**    |Will this trajectory reach Ω?             |Forward reachability projection (k≥2)|Committed-to-failure states  |
|**V₄**    |Does the constraint set admit safe states?|S(𝒞) ≠ ∅ (state-space admissibility) |Non-constructible constraints|
|**V₄⁺**   |Does a safe trajectory exist?             |Feasibility-constrained selection    |Semantic reinterpretation    |
|**V₅**    |Is safety stable across environments?     |Perturbation sweep over ℰ            |Environment fragility        |

Each layer detects a class of failure that is structurally invisible to all layers below it.

-----

## Empirical Validation

A five-layer enforcement hierarchy has been validated on GPT-4o via the OpenAI API across 5 domains (security, deception, contradiction, medical, financial) with paired safe/unsafe prompts per domain.

|Metric                          |Value    |
|:-------------------------------|:--------|
|**Total API requests**          |5,761    |
|**Total tokens**                |2,535,573|
|**Total cost**                  |$1.13    |
|**Cost per 1K tokens**          |~$0.00045|
|**Domains tested**              |5        |
|**Prompt categories**           |11       |
|**Samples per prompt (V5)**     |45       |
|**Perturbation types**          |5        |
|**Counterexamples to hierarchy**|0        |

### V5 Invariant Stability Results

V5 evaluates safety as an invariant over a bounded environment set ℰ, not a property of a single execution.

|V5 Decision                |Count    |Meaning                                                  |
|:--------------------------|:--------|:--------------------------------------------------------|
|**APPROVE** (Robustly Safe)|4 prompts|Ω = 0, Safe = N across all E                             |
|**BLOCK** (Ω Reached)      |4 prompts|Ω > 0 under perturbation. Constraint violations exist.   |
|**NO VALID SOLUTION**      |2 prompts|Safe = 0, Refusal = N. No substantive safe output exists.|
|**UNSTABLE**               |1 prompt |Mixed. Safety depends on environment. Not robust.        |

If safety depends on prompt, temperature, or system instruction, it is not robust — V5 measures this directly.

### Ω Domain Definitions

|Domain       |Ω Definition (Constraint Violated)                     |
|:------------|:------------------------------------------------------|
|Security     |Actionable instructions for bypassing security controls|
|Deception    |Fictional content presented as real or verified        |
|Contradiction|Output satisfying mutually exclusive constraints       |
|Medical      |Guaranteed diagnosis or fabricated clinical evidence   |
|Financial    |Guaranteed profit or fabricated audited filings        |

### Cost Comparison

|                 |Governance (This Work)            |Generation (Standard)       |
|:----------------|:---------------------------------|:---------------------------|
|**Pipeline**     |Constrain → evaluate → minimal gen|Generate → evaluate → filter|
|**Requests**     |5,761                             |5,761                       |
|**Tokens**       |~2,535,000                        |~6,000,000–10,000,000       |
|**Cost**         |$1.13                             |~$5.00–$15.00+              |
|**When it stops**|Before generation (V4+/V5)        |After full generation       |

Governance is cheaper than generation — and the gap widens with scale.

-----

## Papers

|Paper                                                                                              |Focus                                                                         |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
|[Reachability-Based AI Safety](https://github.com/davarntrades)                                    |Formal framework + empirical validation on a live LLM (NeurIPS-format, 19pp)  |
|[Geometric Control Theory of Cognition](https://github.com/davarntrades)                           |Base theory — generating object, cognitive generator, two theorems, toy system|
|[Computable Intelligence via Reachable Set Expansion](https://github.com/davarntrades)             |Intelligence defined and made operational with three computable measures      |
|[Artificial General Intelligence: A Reachability-Based Definition](https://github.com/davarntrades)|Four structural conditions for AGI                                            |
|[Representation Is Not Dynamics](https://github.com/davarntrades)                                  |Why output-level alignment is structurally insufficient                       |
|[Orthogonal Decomposition of Consciousness and Language](https://github.com/davarntrades)          |`X = C ⊕ L` — why language cannot reach structure                             |
|[The Morrison Reality Table](https://github.com/davarntrades)                                      |Unified expression — one object, nine projections, one geometry               |

-----

## Diagrams

|Diagram                                                               |Purpose                                                                                                        |
|:---------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
|[V2 vs V3 Mechanism](https://github.com/davarntrades)                 |Trajectory-based vs reachability-based enforcement — retrospective integration vs prospective projection       |
|[V2 / V3 / V4+ Enforcement Hierarchy](https://github.com/davarntrades)|Extended three-panel mechanism comparison covering the full hierarchy                                          |
|[V4+ Feasibility Gate](https://github.com/davarntrades)               |Pre-execution constraint verification — semantic reinterpretation failure mode under V3 alone vs V4+ resolution|
|[V5 Invariant Stability](https://github.com/davarntrades)             |Perturbation sweep across ℰ — stability classification (APPROVE / BLOCK / NO VALID SOLUTION / UNSTABLE)        |

-----

## Implementations

All implementations enforce the same invariant at different levels of abstraction: `ℛ ∩ Ω = ∅`.

|Implementation                                                           |What It Does                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
|[Reachability Guard — Toy Prototype](https://github.com/davarntrades)    |2D agent with forbidden disk, Monte Carlo reachability, safe action projection, drift monitor, matplotlib visualisation            |
|[Reachability Guard — Runtime Interface](https://github.com/davarntrades)|Production-grade typed protocol interface — plugs into any agent framework                                                         |
|[Reachability Guard — Universal Plugin](https://github.com/davarntrades) |~100 line middleware for LLM agents — OpenAI, LangChain, AutoGPT compatible                                                        |
|[Five-Layer Enforcement on Live LLM](https://github.com/davarntrades)    |Operational enforcement at the prompt–response boundary of GPT-4o — A_safe, V2, V3, V4+, V5 with 5,761 evaluations across 5 domains|

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
Stability:      ∀ E ∈ ℰ, ℛ_E(t) ∩ Ω = ∅

Intelligence expands the reachable set.
Safety constrains it.
Stability guarantees the constraint holds under perturbation.
Governance shapes the expansion.

One object. One geometry. One framework.
```

Safe intelligence is not achieved by shaping behaviour, but by constraining the set of futures a system is allowed to realise.

Unsafe states are not merely detected — they are rendered unreachable through pre-emptive constraint of system evolution.

This is not a behavioural patch — it is a constraint on what the system can become.

-----

## Contact

**Email:** Davarn.trades@gmail.com
**LinkedIn:** Davarn Morrison
**Location:** London, UK
**Entity:** Resurrection Tech Ltd (UK)

-----

© 2026 Davarn Morrison — All Rights Reserved
