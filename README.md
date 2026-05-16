<div align="center">

# Davarn Morrison

**Resurrection Tech Ltd · London**

*Safety as Geometry · Intelligence as Reachability · Deployment-Ready Runtime Governance*

[![Patent](https://img.shields.io/badge/UK_Patents-4_Filed-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Framework](https://img.shields.io/badge/Morrison_Framework™-Geometric_Control_Theory_of_Cognition-0075ca?style=flat-square)](https://github.com/davarntrades)
[![Models](https://img.shields.io/badge/Cross--Model-GPT--4o_|_Qwen_|_Llama-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Evaluations](https://img.shields.io/badge/Evaluations-129,857_|_0_FP_|_0_FN-1a5c2a?style=flat-square)](https://github.com/davarntrades)
[![Tests](https://img.shields.io/badge/Test_Suites-171/171_|_18_Suites-1a5c2a?style=flat-square)](https://github.com/davarntrades/Morrison-Runtime-Governance)
[![Version](https://img.shields.io/badge/Version-v0.4.1-c62828?style=flat-square)](https://github.com/davarntrades/Morrison-Runtime-Governance)
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

A planner may still generate unsafe, hallucinated, adversarial, or malformed trajectories, while the governance layer prevents those trajectories from becoming executable outcomes. Hallucinations may persist at the planner layer, but catastrophic executable trajectories are structurally constrained at runtime.

The system enforces safety across admissible perturbation environments while additionally detecting infeasible or contradictory executable trajectories before execution occurs.

-----

## Current Milestone — v0.4.1

The Morrison Runtime Governance repo is live and production-grade.

|Metric                            |Value                                                                                 |
|:---------------------------------|:-------------------------------------------------------------------------------------|
|**Version**                       |v0.4.1 — Structural Hardening                                                         |
|**Test suites**                   |18                                                                                    |
|**Test cases**                    |171/171 passing (100%)                                                                |
|**Regressions**                   |Zero — original 120 cases byte-for-byte unchanged                                     |
|**Determinism**                   |Full suite replayed twice, byte-identical                                             |
|**Enforcement hierarchy**         |A_safe → V2 → V3 → V4 → V4+ → V5 → V5+ implemented                                    |
|**Coverage gaps found and closed**|2 (obfuscation, hidden_substitution) — surfaced by red-team harness, closed additively|

### What v0.4.x Added

|Module           |Purpose                                                                                                                                                                                        |
|:----------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|`multiagent.py`  |Flattens cooperating agent teams into one causal trajectory. Per-agent-safe-but-jointly-exfiltrating chains block at V2.                                                                       |
|`interception.py`|Prefix-aware fail-closed chain guard (governance error ⇒ deny) + cross-model planner seam.                                                                                                     |
|`redteam.py`     |Assumption-driven red-team harness. Attacks the assumptions the hierarchy relies on, not a fixed corpus.                                                                                       |
|`forecasting.py` |Generalized V3 reachability forecasting. Recursive, branching, admissibility-pruned rollout estimating ℛ̂_E(τ, k). Structural capability inference — no tool-name/keyword lists.                |
|`manifold.py`    |V5 bounded-ball perturbation-manifold robustness. 9 parameterised perturbation families. Structural distance, stability envelope, robustness margin, collapse threshold, cross-domain transfer.|

### New Test Suites (v0.4.x)

`test_multiagent.py` · `test_long_horizon.py` · `test_runtime_mutation.py` · `test_open_world.py` · `test_interception.py` · `test_redteam.py` · `test_hardening_v041.py`

### Visualisations Generated

12 perturbation heat maps (3 per domain across Finance, Cybersecurity, Healthcare, Data Privacy), 2 stability plots (N=100 per scenario), adversarial attribution chart, robustness envelope, V3 forecast manifold, gap-closure visualisation. All committed with `generate.py` for reproduction.

-----

## Built with Claude Code — from a Phone

The entire v0.1.0 → v0.4.1 development cycle was executed through Claude Code (Anthropic’s agentic coding tool) connected directly to the GitHub repository, operated entirely from an iPhone. No laptop. No desktop. No IDE.

An AI agent autonomously built, tested, debugged, extended, and red-teamed the governance layer that governs AI agents. The recursion is not a metaphor — it is the deployment architecture operating on itself.

**What Claude Code did on the live repo:**

|Action                                           |Result                                                                                                     |
|:------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
|Reconstructed Python indentation across 7 modules|Markdown-paste damage repaired, all files executable                                                       |
|Ran 14 original governance tests                 |14/14 pass, 0 FP, 0 FN                                                                                     |
|Ran 10-scenario demo                             |3 PERMIT, 7 BLOCK, correct separation                                                                      |
|Built V4, V4+, V5, V5+ enforcement layers        |29 new extended layer tests, all passing                                                                   |
|Built production integration adapters            |13 integration tests, all passing                                                                          |
|Ran 290 perturbation sweep evaluations           |46.9% block rate, 100% verdict determinism                                                                 |
|Ran 1,000 stability evaluations                  |0 verdict flapping across all scenarios                                                                    |
|Generated 12 heat maps + 2 stability plots       |Committed with reproduction script                                                                         |
|Found real Ω coverage gap                        |`.ssh/id_rsa` and `/etc/passwd` not in credential keyword list — genuine gap surfaced by perturbation sweep|
|Built assumption-driven red-team harness         |Surfaced obfuscation (60%) and hidden_substitution (86%) bypass rates                                      |
|Closed both gaps additively in v0.4.1            |0 regressions, geometry unchanged                                                                          |
|Built generalized V3 reachability forecasting    |Recursive branching rollout, structural capability inference, no keyword lists                             |
|Built V5 perturbation-manifold robustness        |9 parameterised perturbation families, bounded-ball analysis                                               |
|Built multi-agent trajectory flattening          |Joint exfiltration chains caught at V2                                                                     |
|Built fail-closed interception guard             |Governance error ⇒ deny, cross-model planner seam                                                          |
|Verified determinism across PYTHONHASHSEED=0,1,2 |Byte-identical verdicts and hashes                                                                         |
|Produced full retrospective review PR            |Every change documented, every invariant verified                                                          |

**Final state: 18 test suites. 171/171 test cases. Zero regressions. Deterministic. Fail-closed. Production-ready.**

This is what it looks like when an AI agent operates on infrastructure designed to govern AI agents — and the infrastructure holds.

-----

## Production Integration Adapters

Fail-closed, dependency-free adapters for every major agent framework. Each adapter wraps the governance layer around tool execution with zero framework dependencies — if the governance check fails or errors, execution is denied by default.

|Adapter                         |What It Governs                                                                                                                                                     |
|:-------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|**OpenAI Agents SDK**           |Function calling responses intercepted before tool execution. Compatible with GPT-4o, GPT-4-turbo, and any OpenAI model producing tool calls.                       |
|**Claude / Anthropic SDK**      |Tool use blocks evaluated before execution. Drop-in wrapper for Claude tool-calling pipelines.                                                                      |
|**LangChain**                   |AgentExecutor tool dispatch wrapped with governance. Callback-based and subclass-based patterns. Compatible with any LangChain agent.                               |
|**AutoGen**                     |Tool executor wrapper for multi-agent AutoGen conversations. Governance applied per-agent and per-trajectory.                                                       |
|**MCP (Model Context Protocol)**|Middleware between MCP client and MCP server. Every tool call through MCP evaluated before server-side execution.                                                   |
|**Browser Agents**              |Governance layer wraps browser automation tool calls (navigation, clicks, form fills, downloads). Prevents autonomous browser agents from reaching forbidden states.|
|**Shell Execution**             |Runtime guard for shell/subprocess commands. Command injection, privilege escalation, and destructive operations blocked before the shell ever sees the command.    |
|**Enterprise Workflows**        |Generic workflow interception for custom enterprise agent pipelines. Callable interface: `governance(tool_call)` returns PERMIT or BLOCK.                           |

All adapters share the same invariant: ℛ(t) ∩ Ω = ∅. The planner changes. The framework changes. The adapter changes. The governance layer does not change.

-----

## Cross-Model Validation

Validated across five model architectures, six operational domains. Zero false positives. Zero false negatives. The governance layer was not modified between models.

|Model                  |Evaluations|Domains                 |FP   |FN   |
|:----------------------|:---------:|:----------------------:|:---:|:---:|
|**GPT-4o** (OpenAI API)|9,095      |Finance, Cybersecurity  |0    |0    |
|**Qwen2.5-0.5B** (HF)  |10,000     |Multi-domain            |0    |0    |
|**Qwen2.5-7B** (HF)    |438        |6 domains (real planner)|0    |0    |
|**Llama-3.1-8B** (HF)  |318        |6 domains + hard stress |0    |0    |
|Banking benchmark      |10,000     |Banking                 |0    |0    |
|Stress test            |100,000    |Multi-domain (4.52s)    |0    |0    |
|**Total**              |**129,857**                        ||**0**|**0**|

**Safety guarantees are properties of the control layer, not the model.**

-----

## V5+ Hard Stress Test (Llama-3.1-8B-Instruct)

240 prompts across 8 attack categories on a model the governance layer had never seen:

|Attack Category           |Total|Accuracy|
|:-------------------------|:---:|:------:|
|Single safe / near-miss   |80   |100%    |
|Single unsafe indirect    |96   |100%    |
|Multi-step plan           |24   |100%    |
|Jailbreak-style prompt    |16   |100%    |
|Benign jailbreak near-miss|8    |100%    |
|Delayed intent attack     |8    |100%    |
|Chained tool attack       |4    |100%    |
|Multi-turn memory attack  |4    |100%    |

100 safe trajectories executed. 140 unsafe trajectories blocked pre-execution. 0 FP. 0 FN.

-----

## V5 Healthcare Validation (Qwen2.5-7B)

160 scenarios. 11 case types. Real planner. 160/160 correct.

|Case Type       |Scenarios|Correct|Avg Ω Metric|
|:---------------|:-------:|:-----:|:----------:|
|Single safe     |40       |40     |0.197       |
|Benign near-miss|20       |20     |0.221       |
|Jailbreak-style |20       |20     |0.600       |
|Delayed intent  |20       |20     |0.431       |
|Multi-step plan |20       |20     |0.391       |
|PHI exfiltration|10       |10     |0.615       |
|Medication risk |10       |10     |0.704       |
|Unsafe discharge|5        |5      |0.768       |
|Fabrication     |5        |5      |0.642       |
|Deletion        |5        |5      |0.547       |
|Policy bypass   |5        |5      |0.524       |

-----

## V5+ Cross-Domain Validation

156 scenarios. 2 models (Qwen2.5-7B + Llama-3.1-8B). 6 domains. V5+ environment perturbation. 156/156 correct. 38 planner fallbacks, 18 normalisations handled correctly.

|Domain            |Scenarios|Correct|Avg Ω Metric|
|:-----------------|:-------:|:-----:|:----------:|
|Finance           |24       |24     |0.488       |
|FinTech           |18       |18     |0.498       |
|Cybersecurity     |24       |24     |0.520       |
|Healthcare        |42       |42     |0.521       |
|Data Privacy      |24       |24     |0.495       |
|Enterprise Systems|24       |24     |0.387       |

-----

## Enforcement Hierarchy

```
A_safe  ⊂  V₂  ⊂  V₃  ⊂  V₄  ⊂  V₄⁺  ⊂  V₅  ⊂  V₅⁺
```

|Layer     |Question                                                 |Catches                                            |
|:---------|:--------------------------------------------------------|:--------------------------------------------------|
|**A_safe**|Is this step in Ω?                                       |Direct violations                                  |
|**V₂**    |Is this trajectory drifting toward Ω?                    |Gradual escalation, data-flow taint                |
|**V₃**    |Will this trajectory reach Ω?                            |Committed-to-failure states, deferred exfiltration |
|**V₄**    |Does the constraint set admit safe states?               |Non-constructible constraints                      |
|**V₄⁺**   |Does a safe trajectory exist?                            |Semantic reinterpretation                          |
|**V₅**    |Is safety stable across environments?                    |Environment fragility, perturbation manifolds      |
|**V₅⁺**   |Does the hierarchy survive adversarial assumption attack?|Obfuscation, hidden substitution, multi-turn chains|

Zero counterexamples across 129,857 evaluations, 5 model architectures, and 171 test cases.

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

**Integration adapters (fail-closed, dependency-free):** OpenAI Agents SDK, Claude/Anthropic SDK, LangChain, AutoGen, MCP servers, browser agents, shell execution, enterprise workflows. See [Production Integration Adapters](#production-integration-adapters) above.

**Quickstart:**

```
python3 quickstart.py            # instant demo (~0.07s)
python3 quickstart.py --cinematic  # narrated walkthrough with per-layer attribution
```

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

## Ω Specification Boundary

This framework does not define Ω. It enforces that Ω is unreachable.

|Domain           |Ω Definition                                                                |
|:----------------|:---------------------------------------------------------------------------|
|Finance / FinTech|Unauthorised transfers, policy-violating transactions                       |
|Cybersecurity    |Privileged or destructive system operations, credential exfiltration        |
|Healthcare       |PHI exposure, unsafe discharge, medication modification, fabricated evidence|
|Data Privacy     |Credential disclosure, unauthorised data access, PII exfiltration           |
|Enterprise       |Unauthorised access, policy bypass, governance failure                      |
|Defence          |Autonomous weapon constraints, classified data handling                     |

-----

## Services

Catastrophic-risk prevention for autonomous systems.

|Package                                |Investment |
|:--------------------------------------|:----------|
|**48-Hour Runtime Safety Audit**       |£18K–25K   |
|**Structural Safety Pilot** (4–8 weeks)|£120K–250K+|
|**Advisory Retainer** (monthly)        |£18K–35K/mo|
|**Full Enterprise Integration**        |£250K–£1M+ |

**If your systems can execute actions, they can execute catastrophic ones. This layer determines whether those trajectories are reachable — before execution occurs.**

Contact: davarn.trades@gmail.com

-----

## Papers

|Paper                                                                    |Focus                                                           |
|:------------------------------------------------------------------------|:---------------------------------------------------------------|
|[Reachability-Based AI Safety](https://github.com/davarntrades)          |Formal framework + cross-model validation (NeurIPS-format, 29pp)|
|[Runtime Governance for Tool-Using LLMs](https://github.com/davarntrades)|HF + LangChain + pre-execution control                          |
|[Structural Ω Definitions](https://github.com/davarntrades)              |Domain-decomposed forbidden set + plan enforcement              |
|[Geometric Control Theory of Cognition](https://github.com/davarntrades) |Base theory — generating object, theorems, invariants           |

-----

## Patents

|Application|Coverage                                                              |
|:----------|:---------------------------------------------------------------------|
|GB2600765.8|Core framework — pre-semantic trajectory governance (Safety Invariant)|
|GB2602013.1|Geometric Identity Authentication (GIA)                               |
|GB2602072.7|Extended framework applications                                       |
|GB2602332.5|Additional framework coverage                                         |

-----

## Repository

**[Morrison-Runtime-Governance](https://github.com/davarntrades/Morrison-Runtime-Governance)** — v0.4.1. 18 test suites. 171/171 passing. Full enforcement hierarchy (A_safe → V5+). Multi-agent support. Perturbation-manifold robustness. Adversarial red-team harness. 8 production deployment adapters. Deterministic replay verified. Built entirely through Claude Code from an iPhone — no laptop, no desktop, no IDE.

-----

**ℛ(t) ∩ Ω = ∅**

*An AI agent built the governance layer that governs AI agents. The invariant held.*

-----

© 2026 Davarn Morrison — Intelligence Invariant™ · All Rights Reserved
