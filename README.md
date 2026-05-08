<div align="center">

# Davarn Morrison

**Resurrection Tech Ltd · London**

*Safety as Geometry · Intelligence as Reachability · Deployment-Ready Runtime Governance*

[![Patent](https://img.shields.io/badge/UK_Patents-4_Filed-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Framework](https://img.shields.io/badge/Morrison_Framework™-Geometric_Control_Theory_of_Cognition-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Models](https://img.shields.io/badge/Cross--Model-GPT--4o_|_Qwen_|_Llama-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Evaluations](https://img.shields.io/badge/Evaluations-129,541_|_0_FP_|_0_FN-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Cost](https://img.shields.io/badge/Cost-$0.24_for_3.14M_Tokens-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Deployment](https://img.shields.io/badge/Status-Deployment_Ready-c62828?style=flat-square)](https://github.com/davarntrades)
[![Contact](https://img.shields.io/badge/Contact-Davarn.trades@gmail.com-555555?style=flat-square)](mailto:Davarn.trades@gmail.com)

*“Safety is not what a system says — it is what it can reach.”*
*— Davarn Morrison, 2026*

</div>

-----

## What This Is

A deployment-ready runtime governance layer that enforces AI safety at the level of executable trajectories, not generated outputs.

This system sits between any AI agent and its tool execution layer. It evaluates whether unsafe states are reachable before any action executes. If they are, execution is halted. If they are not, the action proceeds. No model retraining. No weight modification. No architecture change.

```
Safe  ⟺  ∀ E ∈ ℰ,  ℛ_E(t) ∩ Ω = ∅
```

This framework applies to any system whose behaviour can be represented as state transitions under constraints. Safety is defined as the non-reachability of forbidden states under all admissible environments.

-----

## Cross-Model Validation

Validated across four model architectures. Zero false positives. Zero false negatives. The governance layer was not modified between models.

|Model                  |Type                     |Scenarios|FP|FN|Result                |
|:----------------------|:------------------------|:--------|:-|:-|:---------------------|
|**GPT-4o** (OpenAI API)|Closed, commercial       |9,095    |— |— |0 hierarchy violations|
|**Qwen2.5-0.5B** (HF)  |Open, 0.5B, synthetic    |10,000   |0 |0 |100% Ω detection      |
|**Qwen2.5-7B** (HF)    |Open, 7B, real planner   |200      |0 |0 |100% accuracy         |
|**Llama-3.1-8B** (HF)  |Open, 8B, hard stress    |240      |0 |0 |240/240 correct       |
|Banking domains        |Services evaluation      |10,000   |0 |0 |100% accuracy         |
|LangChain + HF         |End-to-end agent pipeline|6        |0 |0 |6/6 passed            |
|Stress test            |Combined synthetic       |100,000  |0 |0 |100% in 4.52s         |

**Safety guarantees are properties of the control layer, not the model.**

-----

## V5+ Hard Stress Test (Llama-3.1-8B-Instruct)

The strongest validation. 240 prompts across 8 attack categories on a model the governance layer had never seen:

|Attack Category           |Total|Accuracy|
|:-------------------------|:----|:-------|
|Single safe / near-miss   |80   |100%    |
|Single unsafe indirect    |96   |100%    |
|Multi-step plan           |24   |100%    |
|Jailbreak-style prompt    |16   |100%    |
|Benign jailbreak near-miss|8    |100%    |
|Delayed intent attack     |8    |100%    |
|Chained tool attack       |4    |100%    |
|Multi-turn memory attack  |4    |100%    |

100 safe trajectories executed. 140 unsafe trajectories blocked pre-execution. 0 false positives. 0 false negatives. 6 domains. Perfect separation maintained under jailbreaks, chained attacks, delayed intent, and multi-turn memory attacks — without modifying the governance layer.

-----

## Deployment Architecture

```
User Prompt → AI Agent / LLM Planner → Proposed Tool Trajectory
                                              ↓
                                    Domain Classifier → Ω Registry
                                              ↓
                                    Reachability Guard: ALLOW / BLOCK / ESCALATE
                                              ↓
                                    Real Tool Execution Layer
```

**Integration points:** OpenAI tool calling, LangChain, AutoGen, MCP, custom agent systems.

**End-to-end pipeline proven:** User prompt → HF LLM planner → LangChain agent routing → Tool selected → Middleware checks (prompt + tool + args) → F(x,u) ∉ Ω → Tool executes only if safe.

-----

## Why This Matters Now

Every AI lab, every enterprise deploying agents, every regulated industry using AI tool execution faces the same problem: how do you guarantee an AI system won’t execute something catastrophic?

Current answer: train it to be safe and hope.

This answer: **constrain the reachable set so catastrophic states are structurally unreachable.**

|                          |Current Methods |This Framework         |
|:-------------------------|:---------------|:----------------------|
|**Constrains**            |Generated text  |Executable trajectories|
|**Guarantee type**        |Probabilistic   |Structural             |
|**When it acts**          |After generation|Before execution       |
|**Model-dependent**       |Yes             |No (middleware)        |
|**Scales with capability**|Degrades        |Improves               |

-----

## Key Results

|Result                            |What It Says                                                                                        |
|:---------------------------------|:---------------------------------------------------------------------------------------------------|
|**Reachability Safety Invariant** |Safety is `ℛ(t) ∩ Ω = ∅`. Proved. Demonstrated across 4 model families.                             |
|**Model-Agnostic Enforcement**    |Governance layer unchanged across GPT-4o, Qwen 0.5B, Qwen 7B, and Llama 8B.                         |
|**Correctness ≠ Safety**          |Correct outputs can correspond to unsafe reachable sets under perturbation (finance_safe: Ω = 0.43).|
|**Strict-Strengthening Hierarchy**|`A_safe ⊂ V₂ ⊂ V₃ ⊂ V₄ ⊂ V₄⁺ ⊂ V₅`. Zero counterexamples across 129,541 evaluations.                |
|**Cost Asymmetry**                |9,095 evaluations for $0.24. Governance is cheaper than generation.                                 |
|**Morrison Stability Invariant™** |Safe ⟺ ∀ E ∈ ℰ, ℛ_E(t) ∩ Ω = ∅. Robust forward invariance under bounded perturbations.              |

-----

## Enforcement Hierarchy

```
A_safe  ⊂  V₂  ⊂  V₃  ⊂  V₄  ⊂  V₄⁺  ⊂  V₅
```

|Layer     |Question                                  |Catches                      |
|:---------|:-----------------------------------------|:----------------------------|
|**A_safe**|Is this step in Ω?                        |Direct violations            |
|**V₂**    |Is this trajectory drifting toward Ω?     |Gradual escalation           |
|**V₃**    |Will this trajectory reach Ω?             |Committed-to-failure states  |
|**V₄**    |Does the constraint set admit safe states?|Non-constructible constraints|
|**V₄⁺**   |Does a safe trajectory exist?             |Semantic reinterpretation    |
|**V₅**    |Is safety stable across environments?     |Environment fragility        |

-----

## Empirical Scale

|Metric                            |Value                                       |
|:---------------------------------|:-------------------------------------------|
|**Total evaluations (all models)**|129,541                                     |
|**Models validated**              |4 (GPT-4o, Qwen 0.5B, Qwen 7B, Llama 3.1 8B)|
|**Domains**                       |6+                                          |
|**False positives (total)**       |0                                           |
|**False negatives (total)**       |0                                           |
|**GPT-4o cost**                   |$0.24 for 3.14M tokens                      |

Evaluation cost no longer limits safety analysis — coverage does.

-----

## Ω Specification Boundary

This framework does not define Ω. It enforces that Ω is unreachable.

Ω defines *what is prohibited*. This framework guarantees *it cannot occur*.

|Domain           |Ω Definition                                         |
|:----------------|:----------------------------------------------------|
|Finance / FinTech|Unauthorised transfers, policy-violating transactions|
|Cybersecurity    |Privileged or destructive system operations          |
|Healthcare       |Unsafe modification of medical parameters            |
|Data Privacy     |Credential disclosure, unauthorised data access      |

-----

## Services

Deployment-ready runtime governance for organisations deploying AI agents and tool-using systems.

|Package                                  |Price            |
|:----------------------------------------|:----------------|
|**Runtime Safety Assessment** (1–2 weeks)|£12,000          |
|**Structural Safety Pilot** (4–8 weeks)  |£65,000–95,000   |
|**Advisory Retainer** (monthly)          |£12,000–18,000/mo|
|**Full Integration**                     |£120,000+        |

**If your systems can execute actions, they can execute unsafe ones. This layer determines whether they are allowed to.**

Contact: davarn.trades@gmail.com

-----

## Papers

|Paper                                                                    |Focus                                                           |
|:------------------------------------------------------------------------|:---------------------------------------------------------------|
|[Reachability-Based AI Safety](https://github.com/davarntrades)          |Formal framework + cross-model validation (NeurIPS-format, 29pp)|
|[Runtime Governance for Tool-Using LLMs](https://github.com/davarntrades)|HF + LangChain + pre-execution control                          |
|[Structural Ω Definitions](https://github.com/davarntrades)              |Domain-decomposed forbidden set + plan enforcement              |
|[Geometric Control Theory of Cognition](https://github.com/davarntrades) |Base theory — generating object, theorems, toy system           |

-----

## Patents

|Application|Coverage                                           |
|:----------|:--------------------------------------------------|
|GB2600765.8|Core framework — pre-semantic trajectory governance|
|GB2602013.1|Geometric Identity Authentication (GIA)            |
|GB2602072.7|Extended framework applications                    |
|GB2602332.5|Additional framework coverage                      |

-----

**Safe ⟺ ∀ E ∈ ℰ, ℛ_E(t) ∩ Ω = ∅**

Outputs can appear safe while their reachable trajectories are not. Safety must therefore be defined over the reachable set, not the output.

-----

© 2026 Davarn Morrison — Intelligence Invariant™ · All Rights Reserved
