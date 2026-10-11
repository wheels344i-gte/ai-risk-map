# AI Risk Map — Full Corpus

**Version 1.3 · October 2026 · © 2026 Evan Wheeler · Licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)**

12 domains · 55 categories · 196 risk factors

---

## What this is

A single-page visual reference built to improve the quality of AI risk conversations. Most teams naturally gravitate toward familiar concerns like hallucinations, prompt injection, and bias. But AI risk extends well beyond the usual talking points. The AI Risk Map helps teams quickly widen their perspective, surface blind spots, and identify overlooked risks before moving into deeper analysis.

It is not a risk library or exhaustive catalog. It is a practical tool designed to spark better conversations and uncover overlooked risks.

This file is the machine-readable companion to the poster. It carries every risk factor, plus the scope decisions, source notation, cross-reference reasoning and version history that the poster has no room for.

## What this is NOT

- **Not a scored or ranked risk register.** Position, order, and ID number carry no meaning about likelihood or severity. A rare catastrophic factor sits beside a common minor one.
- **Not a list of well-formed risk statements.** Each entry is a risk *factor* — a condition, failure mode, threat event, or loss event that contributes to risk. In FAIR terms these are not loss-event statements. Scope one properly before using it in analysis.
- **Not exhaustive.** It is a thought-starter. Customize it to your industry, geography, and context.
- **Not a control standard or control library.** Many factors imply a missing or deficient control condition. That is deliberate: a control gap is a condition that contributes to risk. But no factor is phrased as a control to implement, and the map does not say which control closes a gap. One factor may call for several controls, and one control may address several factors. It never names threat actors.
- **Not a replacement for system-specific threat modeling.** It seeds that work; it does not substitute for it.

## Scope boundary — read this before answering coverage questions

**In scope:** risk arising from **your organization's own adoption of AI**.

**Out of scope:** risk arising from **others' adversarial or malicious use of AI against you** — AI-enabled fraud, deepfake impersonation of executives or vendors, adversarial automation of attacks. That risk is real and growing, but it belongs on the enterprise threat and cyber register, not on an adoption map. The effect of competitors' and customers' AI on the value of your own strategy is in scope.

This is a boundary of *subject*, not of degree. AI-enabled phishing is unambiguously amplified by AI and is still out of scope. Do not infer that it is covered.

## Design principles — how factors were admitted and how to read them

These are the rules the map was built by. Use them to judge whether something belongs on the map, and to read the factors and markers correctly.

- **Incremental-risk lens.** Within that boundary, only risks AI introduces or amplifies. Generic IT, cyber, and vendor risk that exists identically without AI stays off.
- **Three retention gates.** A factor earns its place if it clears ANY one: (A) AI-specific: remove AI and the risk vanishes; (B) management delta: the risk is not new, but the way it must be managed is; (C) corroboration: two or more independent AI standards name it.
- **Gate B bounding principle.** The management delta must be specific and nameable, not merely 'there is more of it'. 'Agent-framework sprawl outpacing credential governance' qualifies; 'cyber risk went up' does not.
- **Admission vs. priority.** Passing a gate is admission, not priority. When there were more good candidates than the page could hold, the tiebreak was how likely a competent team is to overlook the factor.
- **Owner-based axis.** Domains are organized by who owns the risk, not by AI lifecycle.
- **What a risk factor is.** A condition, failure mode, or event that contributes to risk. It may imply a missing or deficient control condition, but it is never phrased as a control to implement ('implement MFA') and never as a threat actor ('an attacker'). A proposal that arrives as a control is inverted into the condition it prevents, then checked against neighboring factors before it is added or declined. A factor names what produces a loss, not the impact itself: 'energy use not weighed in deployment choices', not 'environmental footprint'.
- **Split routing rule.** When a risk has an attack side and a condition side owned by different functions, the attack side routes to Security or Autonomy and the condition side to the function that owns it. Whether the two are then a split pair or a see-also depends on the counting test under Cross-reference markers.
- **Cross-reference markers.** »n on the poster (→n in the X-ref column) means this factor is one side of a SPLIT PAIR whose other side is owned by domain n: the same loss seen from two owners' columns; count it once. The test: would assessing both factors as separate scenarios count the same loss twice? The marker is used for nothing else. Both sides of every pair are marked; the Cross-references sheet lists every factor ID on each side. SEE-ALSO POINTERS link different risks worth reading together (a more general factor; the mirror image of the same behavior; the same kind of loss arising a different way; a parallel instance; or a missing safeguard and the risk it protects against); count both. They are listed on the Cross-references sheet and carry no poster marker.

## Identifiers

Every factor carries a permanent ID (`AIRM-001` onward; 196 active). IDs are flat, opaque and sequential. They encode nothing — not domain, not category, not priority. An ID is stable across versions; **the wording of a factor is not**. Cite the ID, not the sentence.

## How to read the Source(s) field

| Notation | Meaning |
|---|---|
| `NAME 0.0` | Traces to a specific numbered element in that source (e.g. `DASF 5.1`, `EU Art 14`, `OWASP LLM01`). |
| `NAME` | The concept appears in that source at section or theme level, not as one numbered element. |
| `Original` | Authored for this map. No reviewed framework names it. |
| `NAME; Original` | The concept traces to that source; the framing and wording are ours. Named sources are listed first, `Original` always last. |

Structure follows an established convention for one-page enterprise risk maps (three tiers, organized by who owns the risk, incremental-risk lens). Format inspiration only — all AI risk content is original or traced to the sources listed.


---

## Using this file with an AI assistant

Paste or upload this whole file, then instruct your assistant as follows.

```
You are helping me use the AI Risk Map. Follow these rules:

1. Answer ONLY from this document. Do not add risks from your own
   knowledge, and do not infer that something is covered because it
   sounds similar to something that is.
2. Cite the AIRM ID for every factor you reference.
3. If something is not covered, say so plainly. Then check the
   "Scope decisions" section — if it was deliberately excluded,
   quote that reasoning.
4. Do not score, rank, rate, or quantify anything. This document
   contains no likelihood or severity data.
5. Before flagging two factors as duplicates, check the
   "Cross-references" section. A split pair (marked →n) is the same
   loss seen from two owners' columns and is split on purpose: count
   it once. A see-also pointer links two different risks: count both.
6. Many factors imply a missing or deficient control condition, but
   this document does not say which control closes a gap. If you
   suggest controls, say they are your suggestions, not the map's.
7. Your job is to widen my thinking, not narrow it. When I describe
   a system or a decision, surface the factors I have not considered
   yet, including ones from domains outside my own function.
8. If I cite an ID marked retired, say so and give the surviving ID.
   If I am working from an earlier version, check the Change log:
   rows marked NARROWED say where the old meaning now lives.
```

**Questions this file answers well:**

- "We're deploying a customer-facing agent. Walk me through the factors we should discuss, domain by domain."
- "Is *X* covered? If not, was it deliberately excluded, and why?"
- "Show me everything Legal owns. Now everything Finance owns."
- "Which factors are split pairs I might double-count?"
- "We just had this incident. Which factors does it touch?"
- "We mapped our controls to an earlier version. What changed that affects the mapping?"
- "Which of these factors would a security team typically miss?"

**Questions it cannot answer:** anything about likelihood, cost, severity, maturity, or control effectiveness. That data is not here by design.


---

## The taxonomy


## 1. AI Governance & Accountability


### Governance & oversight

- **`AIRM-001`** — Inadequate executive/board oversight of AI adoption and risk  
  <sub>Source: NIST Govern; ISO A.2</sub>
- **`AIRM-002`** — Ungoverned ‘shadow AI’ adoption outside sanctioned channels  *(pointed to by `AIRM-104`, Domain 7)*  
  <sub>Source: NIST Govern; CRI GV-1.6.3; COSO GenAI 2026; Original</sub>
- **`AIRM-003`** — Absence of an AI governance body or charter with a clear mandate  
  <sub>Source: ISO A.3</sub>

### Roles & accountability

- **`AIRM-004`** — Unclear ownership and accountability (RACI) for AI risk decisions  *(see also `AIRM-005`, Domain 1 (kept separate on purpose) — count both)*  
  <sub>Source: NIST Govern; ISO A.3</sub>
- **`AIRM-005`** — No clear executive owner for AI adoption: responsibility for strategy, prioritization, and integration into the business diffuses across technology, data science, and business leaders, with no convention for who decides  *(pointed to by `AIRM-004`, Domain 1 (kept separate on purpose))*  
  <sub>Source: Original</sub>
- **`AIRM-006`** — Failure to define accountability for autonomous / agent-driven decisions — internally, and across the AI stack of model provider, platform, developer, and deployer, where the allocation shifts as autonomy increases  *(split pair: other side in Domain 12, `AIRM-187` — count once; pointed to by `AIRM-109`, Domain 7 (missing safeguard))*  
  <sub>Source: EU Art 14; EU Art 25 (amended 2026); CSA AICM; CoSAI AI SRF</sub>
- **`AIRM-007`** — Segregation of duties collapses where the same person or agent configures the AI, operates it, and reviews its output  *(see also `AIRM-175`, Domain 12 — count both)*  
  <sub>Source: COSO GenAI 2026; OWASP AISVS AC.8</sub>

### Policy & standards

- **`AIRM-008`** — Absence of an AI acceptable-use policy and model-approval gates  
  <sub>Source: ISO A.2; NIST Govern</sub>
- **`AIRM-009`** — AI policies not kept current with evolving capabilities and regulation  
  <sub>Source: ISO A.2; Original</sub>
- **`AIRM-010`** — Inconsistent standards across business units, as AI adoption proliferates independently faster than central standards can follow  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-011`** — No agreed definition of what counts as ‘AI’, leaving policy scope, inventory boundaries, and regulatory classification undefined  
  <sub>Source: CRI FS-AI-RMF GV-1.2.2</sub>

### Risk-management integration

- **`AIRM-012`** — AI risk not integrated into enterprise risk management (ERM)  
  <sub>Source: NIST Govern; CRI MG-1.2.1; Original</sub>
- **`AIRM-013`** — Failure to conduct AI impact assessments for individuals and society  
  <sub>Source: EU Art 27 (amended 2026); ISO A.5</sub>
- **`AIRM-014`** — No defined risk appetite or tolerance thresholds for AI  
  <sub>Source: NIST Govern; CRI GV-2.3.2; Original</sub>

### Audit & assurance

- **`AIRM-015`** — Inability to audit AI due to a missing or incomplete inventory of models, agents, and connectors, and their lineage  *(see also `AIRM-063`, Domain 4 (parallel) — count both)*  
  <sub>Source: ISO A.4; NIST Govern; CRI GV-1.6.1</sub>
- **`AIRM-016`** — Insufficient internal-audit competence to assess AI controls  
  <sub>Source: Original</sub>
- **`AIRM-017`** — Absence of independent assurance over AI control effectiveness  *(pointed to by `AIRM-123`, Domain 7)*  
  <sub>Source: CRI GV-1.5.4; Original</sub>
- **`AIRM-018`** — AI output relied upon as evidence in financial-reporting or other regulated control chains without recognizing the expansion of assurance scope  *(see also `AIRM-138`, Domain 8 — count both)*  
  <sub>Source: COSO GenAI 2026 p.13</sub>
- **`AIRM-019`** — No reliable way to identify which artifacts, code, or analyses were AI-generated, so a systemic model or prompt flaw cannot be scoped or remediated after the fact  
  <sub>Source: OWASP AISVS AC.9 / AC.10; COSO GenAI 2026 (AI bill of materials)</sub>

## 2. Strategy & Value Realization


### Competitive position

- **`AIRM-193`** — Advantages built on knowledge, data, or skilled work lose their value as competitors, and even customers, approximate them with general-purpose AI, faster and more cheaply than earlier automation allowed, and our own adoption of AI does not restore the advantage  
  <sub>Source: Original</sub>
- **`AIRM-194`** — Third-party AI assistants and agents increasingly stand between the organization and its customers, searching, comparing, and choosing on the customer's behalf, so the organization loses direct access to the customer, brand preference counts for less, and its offering is compared as a commodity  
  <sub>Source: Original</sub>
- **`AIRM-026`** — Failure to weigh the competitive risk of not adopting AI (inaction)  
  <sub>Source: Databricks AIGF; Cloud Risk Map analog; Original</sub>

### AI strategy & roadmap

- **`AIRM-020`** — Lack of a coherent AI strategy aligned to objectives and risk appetite  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-021`** — AI adoption driven by hype rather than demonstrated business value  *(split pair: other side in Domain 11, `AIRM-167` — count once)*  
  <sub>Source: Original</sub>
- **`AIRM-022`** — Inability to adapt the roadmap as foundation-model capabilities shift  
  <sub>Source: Original</sub>

### Use-case selection & sourcing

- **`AIRM-023`** — Selection of use cases without a clearly defined problem and success measure, or without weighing incremental risk against benefit  
  <sub>Source: CRI MP-3.2.1; Original</sub>
- **`AIRM-024`** — ‘Pilot purgatory’ — pilots stalling on data readiness, evaluation difficulty, or inability to demonstrate value  *(split pair: other side in Domain 11, `AIRM-167` — count once)*  
  <sub>Source: Original</sub>
- **`AIRM-025`** — Misjudged AI sourcing fork — train, fine-tune, retrieval-augment, or call an API — each carrying a different risk and obligation profile  *(see also `AIRM-129`, Domain 8 — count both)*  
  <sub>Source: Original</sub>

### Value measurement / ROI

- **`AIRM-027`** — Unrealistic ROI expectations, where AI benefits are diffuse, hard to attribute, or depend on redesigning workflows around the AI rather than adding it to existing ones  
  <sub>Source: Original</sub>
- **`AIRM-028`** — Inability to attribute value actually delivered by AI investments  
  <sub>Source: Original</sub>
- **`AIRM-029`** — Hidden total cost of ownership (data, talent, integration) eroding returns  *(see also `AIRM-165`, Domain 11 — count both)*  
  <sub>Source: Databricks AIGF; CRI MP-3.2.2; Original</sub>

## 3. Data & Privacy


### Sourcing & provenance

- **`AIRM-030`** — Unknown or undocumented provenance of training / grounding data  
  <sub>Source: NIST GenAI #10; DASF 1.6</sub>
- **`AIRM-031`** — Reliance on data scraped without lawful basis or clear rights  
  <sub>Source: EU Art 10 (amended 2026); NIST Map</sub>
- **`AIRM-032`** — Inadequate data lineage to trace data through the AI pipeline  
  <sub>Source: DASF 1.6</sub>

### Quality & labeling

- **`AIRM-033`** — Poor data quality undermining model reliability  
  <sub>Source: DASF 1.3</sub>
- **`AIRM-034`** — Inadequate or biased labeling introducing systematic error  
  <sub>Source: Original</sub>
- **`AIRM-035`** — Stale data, including grounding and retrieval sources that drift out of date behind a confident-sounding model  
  <sub>Source: DASF 1.9</sub>

### Privacy & consent

- **`AIRM-036`** — Personal data used for training without consent or purpose limitation  *(pointed to by `AIRM-142`, Domain 9 (mirror image); pointed to by `AIRM-069`, Domain 5 (different cause))*  
  <sub>Source: EU Art 10 (amended 2026); NIST GenAI #4</sub>
- **`AIRM-037`** — Inability to honor data-subject rights once data is in a model  
  <sub>Source: GDPR; DASF 1.8; Original</sub>
- **`AIRM-038`** — Re-identification of individuals from aggregated or model-derived data  *(pointed to by `AIRM-069`, Domain 5 (different cause))*  
  <sub>Source: MIT 2.1</sub>
- **`AIRM-039`** — Inadvertent disclosure of confidential / personal data in model output (no output guardrails)  *(pointed to by `AIRM-085`, Domain 5; pointed to by `AIRM-069`, Domain 5 (different cause))*  
  <sub>Source: OWASP LLM02; DASF 10.6</sub>
- **`AIRM-040`** — Sensitive or regulated data used in AI without classification, so handling and access controls are not applied  
  <sub>Source: Databricks AIGF; ISO A.7</sub>
- **`AIRM-041`** — Users pasting confidential or client data into a sanctioned AI tool, moving data outside its control boundary despite upstream access controls working  
  <sub>Source: OWASP AISVS AC.3; COSO GenAI 2026; Original</sub>

### Training-data rights & IP

- **`AIRM-042`** — Use of copyrighted or licensed material in training without rights  *(split pair: other side in Domain 8, `AIRM-131` — count once; see also `AIRM-132`, Domain 8 (parallel) — count both)*  
  <sub>Source: NIST GenAI #10; EU Art 53(1)(c) (amended 2026)</sub>
- **`AIRM-043`** — Contamination of datasets with third-party IP or trade secrets  *(split pair: other side in Domain 8, `AIRM-131` — count once)*  
  <sub>Source: Original</sub>
- **`AIRM-044`** — Inability to prove the organization held the rights to the training data it used  *(see also `AIRM-131`, Domain 8 (missing safeguard) — count both)*  
  <sub>Source: OWASP AISVS 1.1.2; DASF 1.8; Original</sub>

### Retention & disposal

- **`AIRM-045`** — Failure to preserve prompts, outputs, and agent traces subject to litigation hold or e-discovery  *(see also `AIRM-130`, Domain 8 — count both)*  
  <sub>Source: Cloud Risk Map analog; Original</sub>
- **`AIRM-046`** — Inadequate retention / disposal, where deletion from source systems does not remove data already absorbed into models, embeddings, or caches  
  <sub>Source: DASF 1.8; ISO A.7; Original</sub>
- **`AIRM-047`** — Persistence of sensitive data in embeddings, caches, or model weights  *(pointed to by `AIRM-182`, Domain 12 (parallel))*  
  <sub>Source: OWASP LLM08; DASF 1.8; Original</sub>
- **`AIRM-048`** — Failure to remove data across distributed / replicated AI stores  
  <sub>Source: Original</sub>

## 4. Model Development & Performance


### Design & training

- **`AIRM-049`** — Inappropriate model/algorithm choice for the problem and risk context  
  <sub>Source: Original</sub>
- **`AIRM-050`** — Poorly documented or untracked model development  
  <sub>Source: DASF 5.1</sub>
- **`AIRM-051`** — Insecure or unmanaged hyperparameters and training configuration  
  <sub>Source: DASF 5.3</sub>

### Accuracy & validation

- **`AIRM-052`** — Fluent but factually incorrect output (hallucination) accepted as reliable  *(split pair: other side in Domain 6, `AIRM-091` — count once; pointed to by `AIRM-081`, Domain 5)*  
  <sub>Source: NIST GenAI #2; DASF 9.8</sub>
- **`AIRM-053`** — Validation/evaluation data not representative of real-world use, so performance can only be established once real users are exposed, as in pilots and phased rollouts  
  <sub>Source: DASF 6.2; MAS AIRG fn 28 / fn 45</sub>
- **`AIRM-054`** — Skipped or insufficient pre-deployment red-teaming / safety evaluation  
  <sub>Source: EU Art 9; NIST Measure</sub>
- **`AIRM-055`** — Absence of independent model validation / effective challenge  
  <sub>Source: SR 11-7; CRI MS-2.5.1; Original</sub>

### Robustness & drift

- **`AIRM-056`** — Model drift degrading performance as data / conditions change  *(see also `AIRM-108`, Domain 7 (missing safeguard) — count both; see also `AIRM-110`, Domain 7 (missing safeguard) — count both)*  
  <sub>Source: DASF 5.2</sub>
- **`AIRM-057`** — Lack of robustness to edge cases and distribution shift  *(see also `AIRM-197`, Domain 5 (different cause) — count both)*  
  <sub>Source: NIST Measure</sub>
- **`AIRM-058`** — Small changes to the input produce very different output  *(see also `AIRM-197`, Domain 5 (different cause) — count both)*  
  <sub>Source: Original</sub>

### Explainability

- **`AIRM-059`** — Black-box models used in high-stakes decisions without interpretability  
  <sub>Source: NIST Measure; EU Art 13; DASF 6.3</sub>
- **`AIRM-060`** — Inability to produce adverse-action / decision explanations  
  <sub>Source: EU Art 86; Colorado SB 26-189; CRI MS-2.9.2; DASF 6.3; Original</sub>
- **`AIRM-061`** — Over-reliance on post-hoc explanations that misrepresent the model  
  <sub>Source: Original</sub>

### Reproducibility & documentation

- **`AIRM-062`** — Non-reproducible training pipelines undermining validation and audit  
  <sub>Source: DASF 5.1; Original</sub>
- **`AIRM-063`** — Inadequate model documentation / model cards  *(pointed to by `AIRM-015`, Domain 1 (parallel))*  
  <sub>Source: EU Art 11 (amended 2026); NIST Map</sub>
- **`AIRM-064`** — Loss of traceability between model versions, data, and results  
  <sub>Source: DASF 4.1</sub>

## 5. Security & Adversarial Threats


### Data & pipeline attacks

- **`AIRM-065`** — Training-data poisoning that degrades or backdoors model behavior  *(pointed to by `AIRM-122`, Domain 7 (different cause))*  
  <sub>Source: DASF 3.1; OWASP LLM04; ATLAS AML.T0020</sub>
- **`AIRM-066`** — Tampering with RAG / knowledge-base sources consumed at inference  
  <sub>Source: OWASP LLM08; DASF 9.9</sub>
- **`AIRM-067`** — Label-flipping or adversarial dataset partitioning to skew outputs  
  <sub>Source: DASF 3.3 / 2.4</sub>

### Model attacks

- **`AIRM-068`** — Model extraction / theft via inference-API querying  
  <sub>Source: DASF 8.2; ATLAS AML.T0024.002</sub>
- **`AIRM-069`** — Membership-inference or model-inversion exposing training data  *(see also `AIRM-036`, Domain 3 (different cause) — count both; see also `AIRM-038`, Domain 3 (different cause) — count both; see also `AIRM-039`, Domain 3 (different cause) — count both)*  
  <sub>Source: DASF 9.2 / 9.5; NIST GenAI #4</sub>
- **`AIRM-070`** — Backdoored / trojaned pre-trained model from a public hub  
  <sub>Source: DASF 7.1</sub>

### Inference-time (input) attacks

- **`AIRM-071`** — Direct prompt injection altering behavior or bypassing guardrails  
  <sub>Source: OWASP LLM01; DASF 9.1</sub>
- **`AIRM-072`** — Indirect / cross-domain prompt injection via retrieved content  
  <sub>Source: OWASP LLM01; DASF 9.1 / 9.9</sub>
- **`AIRM-073`** — Jailbreaks defeating safety controls and restrictions  *(split pair: other side in Domain 6, `AIRM-097` — count once; see also `AIRM-090`, Domain 6 (different cause) — count both)*  
  <sub>Source: OWASP LLM01; DASF 9.12</sub>
- **`AIRM-074`** — System-prompt leakage exposing operational instructions  
  <sub>Source: OWASP LLM07</sub>
- **`AIRM-197`** — Inputs crafted so a model misclassifies or misses what it is meant to catch, such as fraud, malware, or content and identity checks, without touching the model or its data  *(pointed to by `AIRM-057`, Domain 4 (different cause); pointed to by `AIRM-058`, Domain 4 (different cause))*  
  <sub>Source: ATLAS AML.T0015; ATLAS AML.T0043; NIST AI 100-2 E2025; Original</sub>

### Output & integration security

- **`AIRM-075`** — Unsanitized output reaching downstream interpreters (code exec / XSS / SQLi)  
  <sub>Source: OWASP LLM05</sub>
- **`AIRM-076`** — Interception or manipulation of the inference output stream  
  <sub>Source: DASF 10.2</sub>
- **`AIRM-077`** — Over-trusted output triggering unsafe automated actions  *(see also `AIRM-099`, Domain 6 (different cause) — count both)*  
  <sub>Source: OWASP LLM05 / LLM06</sub>

### Supply-chain & artifact integrity

- **`AIRM-078`** — Compromised or malicious model / component from the AI supply chain  *(split pair: other side in Domain 9, `AIRM-148` — count once; pointed to by `AIRM-189`, Domain 9 (missing safeguard))*  
  <sub>Source: OWASP LLM03; NIST GenAI #12</sub>
- **`AIRM-079`** — Known vulnerabilities in ML dependencies and libraries left unpatched  *(see also `AIRM-149`, Domain 9 (different cause) — count both)*  
  <sub>Source: OWASP LLM03</sub>
- **`AIRM-080`** — Tampering with model artifacts, prompts, or agent configuration in registries or during deployment  *(see also `AIRM-148`, Domain 9 (parallel) — count both; pointed to by `AIRM-124`, Domain 7 (different cause))*  
  <sub>Source: DASF 7.3; ATLAS AML.T0010.004; Original</sub>
- **`AIRM-081`** — Model-invented package, image, or endpoint names that resolve to adversary-registered artifacts, because the same hallucination recurs across users and model families  *(see also `AIRM-052`, Domain 4 — count both)*  
  <sub>Source: OWASP AISVS AC.13</sub>

### AI access & identity

- **`AIRM-082`** — Inadequate access controls on serving endpoints and inference APIs  *(see also `AIRM-178`, Domain 12 (parallel) — count both)*  
  <sub>Source: DASF 9.11</sub>
- **`AIRM-083`** — Over-privileged service accounts and keys for AI platform components (distinct from an agent's tool scope)  *(see also `AIRM-178`, Domain 12 (parallel) — count both; see also `AIRM-177`, Domain 12 (parallel) — count both)*  
  <sub>Source: DASF 1.1; Original</sub>
- **`AIRM-084`** — Insecure storage / exposure of credentials and tokens, as AI tool, harness, and agent-framework sprawl outpaces credential governance  
  <sub>Source: DASF 13.19 / 13.27</sub>
- **`AIRM-085`** — Retrieval and RAG pipelines serving content beyond the requesting user’s own entitlements, because authorization is applied when the index is built rather than when it is queried  *(see also `AIRM-039`, Domain 3 — count both)*  
  <sub>Source: OWASP AISVS 5.2.2</sub>
- **`AIRM-196`** — Insiders direct a sanctioned AI assistant or agent, within its broad access, to find, aggregate, or move data or take actions beyond their own entitlements, with the activity attributed to the agent rather than the person  *(pointed to by `AIRM-178`, Domain 12 (different cause))*  
  <sub>Source: OWASP ASI T3; Original</sub>

## 6. Safety, Ethics & Responsible AI


### Bias & fairness

- **`AIRM-086`** — Discriminatory or biased outputs causing disparate impact  
  <sub>Source: NIST GenAI #6; Weidinger I; Shelby</sub>
- **`AIRM-087`** — Inequitable performance or accessibility across languages, demographics, and disabilities, marginalizing underrepresented groups  
  <sub>Source: MIT 1.3; Shelby QoS; Original</sub>
- **`AIRM-088`** — Bias amplification / homogenization from feedback and scale  
  <sub>Source: NIST GenAI #6</sub>
- **`AIRM-089`** — Culturally insensitive or inappropriate output, or erosion of local norms, when AI is scaled across regions  
  <sub>Source: Databricks AIGF</sub>

### Harmful / inaccurate output

- **`AIRM-090`** — Generation of toxic, dangerous, or hateful content  *(pointed to by `AIRM-073`, Domain 5 (different cause))*  
  <sub>Source: NIST GenAI #3; Weidinger I</sub>
- **`AIRM-091`** — Harmful, misleading, or defamatory output driving decisions  *(split pair: other side in Domain 4, `AIRM-052` — count once)*  
  <sub>Source: NIST GenAI #2; Original</sub>
- **`AIRM-092`** — Harm to minors / vulnerable users from inappropriate output  
  <sub>Source: NIST GenAI #11; Colorado HB 26-1263</sub>

### Transparency, disclosure & provenance

- **`AIRM-093`** — Failure to disclose to users that they are interacting with AI  
  <sub>Source: EU Art 50 (amended 2026); Weidinger V</sub>
- **`AIRM-094`** — Undisclosed synthetic media / deepfakes lacking provenance  
  <sub>Source: EU Art 50 (amended 2026); NIST GenAI #8</sub>
- **`AIRM-095`** — Inadequate transparency to affected parties about AI's role  
  <sub>Source: EU Art 13; ISO A.8</sub>
- **`AIRM-192`** — Changes to the model, prompts, or guardrails behind an AI-powered service we provide, made without notice to the customers and deployers who depend on it, so their validations, disclosures, and controls silently go stale  
  <sub>Source: EU Art 13; EU Art 25 (amended 2026); NIST GenAI #12</sub>

### Misuse & dual-use

- **`AIRM-096`** — Misuse of AI for disinformation, fraud, or social engineering  
  <sub>Source: NIST GenAI; Weidinger IV; IAISR</sub>
- **`AIRM-097`** — Dangerous-capability uplift: the model gives meaningful help toward chemical, biological, radiological, nuclear, or cyber attack capability  *(split pair: other side in Domain 5, `AIRM-073` — count once)*  
  <sub>Source: NIST GenAI #1; Weidinger IV; IAISR</sub>
- **`AIRM-098`** — AI optimized for a proxy measure (engagement, conversion, or revenue) that diverges from users' interests, driving addiction, polarization, or unsuitable recommendations  
  <sub>Source: Shelby societal; MAS AIRG §1.9(c); Original</sub>

### Human agency & over-reliance

- **`AIRM-099`** — User over-trust / automation bias in AI outputs  *(pointed to by `AIRM-077`, Domain 5 (different cause))*  
  <sub>Source: NIST GenAI #7; Weidinger V</sub>
- **`AIRM-100`** — Anthropomorphism and emotional dependence on conversational AI  
  <sub>Source: Weidinger V; Colorado HB 26-1263</sub>
- **`AIRM-101`** — Erosion of meaningful human control over decisions  *(see also `AIRM-176`, Domain 12 (missing safeguard) — count both)*  
  <sub>Source: EU Art 14; MIT 5.2</sub>
- **`AIRM-102`** — Human review, approval, and triage capacity cannot scale to the volume AI produces — code, alerts, content, decisions — so oversight gates degrade into rubber-stamping while still appearing effective  *(see also `AIRM-117`, Domain 7 — count both)*  
  <sub>Source: COSO GenAI 2026; OWASP AISVS AC.4; CRI MP-3.5.4</sub>

## 7. Operations & Resilience


### MLOps & deployment

- **`AIRM-103`** — Immature MLOps / fragile deployment pipelines  
  <sub>Source: DASF 11.1; Original</sub>
- **`AIRM-104`** — Inconsistent or unsanctioned (shadow) model deployment  *(see also `AIRM-002`, Domain 1 — count both)*  
  <sub>Source: DASF 8.3; Original</sub>
- **`AIRM-105`** — Inadequate environment and configuration management across model versions, dependency pinning, and accelerator configuration, undermining reproducibility  
  <sub>Source: DASF 12.5</sub>
- **`AIRM-106`** — Training-serving skew: features or input data differ between training and production, degrading live performance  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-107`** — Containment of an AI test, evaluation, or development environment fails — unverified, misconfigured, defeated, or degraded over time — allowing the system to reach production or third-party systems  *(see also `AIRM-174`, Domain 12 — count both)*  
  <sub>Source: OpenAI/Anthropic 2026 incidents</sub>

### Monitoring & observability

- **`AIRM-108`** — Absence of monitoring for performance, drift, and abuse in any environment — including evaluation, test, and sandbox environments assumed to be contained  *(pointed to by `AIRM-056`, Domain 4 (missing safeguard))*  
  <sub>Source: DASF 10.1; NIST Manage; CSA HF post-mortem</sub>
- **`AIRM-109`** — Inadequate logging / audit of inputs, outputs, tool calls, agent decision paths, and the human authorization behind them  *(see also `AIRM-187`, Domain 12 — count both; see also `AIRM-006`, Domain 1 (missing safeguard) — count both)*  
  <sub>Source: EU Art 12; DASF 10.1</sub>
- **`AIRM-110`** — Inability to detect anomalous or degraded behavior, where non-determinism makes 'anomalous' hard to define and baseline  *(pointed to by `AIRM-056`, Domain 4 (missing safeguard))*  
  <sub>Source: DASF 10.1; Original</sub>
- **`AIRM-111`** — Sanctioned agent activity indistinguishable from agentic attack in telemetry  
  <sub>Source: CSA HF post-mortem</sub>

### Availability & scalability

- **`AIRM-112`** — Inference latency or unavailability degrading dependent services  *(see also `AIRM-170`, Domain 11 (different cause) — count both)*  
  <sub>Source: Databricks AIGF; CSA AICM; Original</sub>
- **`AIRM-113`** — Inability to scale inference to peak demand  *(see also `AIRM-170`, Domain 11 (different cause) — count both; see also `AIRM-165`, Domain 11 (different cause) — count both)*  
  <sub>Source: Original</sub>
- **`AIRM-114`** — Deliberate resource exhaustion or denial-of-wallet: requests crafted to run up AI compute costs or exhaust capacity  *(see also `AIRM-164`, Domain 11 (different cause) — count both)*  
  <sub>Source: OWASP LLM10</sub>

### Incident management

- **`AIRM-115`** — Immature AI incident response and escalation processes  
  <sub>Source: NIST Manage; CRI GV-4.3.2; DASF 12.3; Original</sub>
- **`AIRM-116`** — Inability to investigate AI incidents due to non-determinism / poor logs  
  <sub>Source: DASF 12.3; CRI MS-2.4.4; Original</sub>
- **`AIRM-117`** — Inadequate content-moderation / trust-&-safety operations at scale  *(pointed to by `AIRM-102`, Domain 6)*  
  <sub>Source: Colorado HB 26-1263; Original</sub>
- **`AIRM-118`** — Safety guardrails on models relied on for defense refusing to assist incident response, blocking analysis of attack data  
  <sub>Source: CSA HF post-mortem</sub>

### Change & lifecycle management

- **`AIRM-119`** — Silent vendor / model updates changing behavior without notice  *(see also `AIRM-141`, Domain 9 — count both)*  
  <sub>Source: COSO GenAI 2026; OWASP AISVS 3.2.3; Original</sub>
- **`AIRM-120`** — Inadequate versioning, rollback, and change control for models  *(pointed to by `AIRM-141`, Domain 9)*  
  <sub>Source: DASF 8.3; CRI MG-4.1.4; Original</sub>
- **`AIRM-121`** — Unmanaged model decommissioning / sunset leaving orphaned dependencies  
  <sub>Source: CRI GV-1.7.1; CRI MG-2.4.2; Original</sub>
- **`AIRM-122`** — Uncontrolled continuous or online learning, where the model keeps changing in production without validation, introducing drift  *(see also `AIRM-065`, Domain 5 (different cause) — count both)*  
  <sub>Source: DASF 5.2; Original</sub>
- **`AIRM-123`** — Guardrails, access scopes, and approval gates re-verified less often than the AI system's capability and integration surface changes  *(see also `AIRM-017`, Domain 1 — count both)*  
  <sub>Source: 2026 sandbox-escape incidents; Original</sub>
- **`AIRM-124`** — Prompts, system prompts, and retrieval configuration changed outside change control, though they determine system behavior as directly as code  *(see also `AIRM-080`, Domain 5 (different cause) — count both)*  
  <sub>Source: COSO GenAI 2026 Principle 11; OWASP AISVS AC.11</sub>

## 8. Legal, Regulatory & Compliance


### Regulatory compliance

- **`AIRM-125`** — Unknowingly deploying a prohibited or high-risk AI use case  
  <sub>Source: EU Art 5 / Annex III</sub>
- **`AIRM-126`** — Failure to meet high-risk obligations (risk mgmt, docs, oversight)  
  <sub>Source: EU Arts 9-15</sub>
- **`AIRM-127`** — Inability to keep pace with fragmented, fast-changing AI regulation  
  <sub>Source: Colorado SB 26-189; CRI GV-1.1.1; Databricks AIGF; Original</sub>
- **`AIRM-128`** — User inability to contest or seek recourse on an AI-driven decision  
  <sub>Source: EU Arts 85 / 86; Colorado SB 26-189</sub>
- **`AIRM-129`** — Misclassifying the organization's regulatory role (deployer vs. provider), missing obligations triggered by fine-tuning or rebranding a model  *(pointed to by `AIRM-025`, Domain 2)*  
  <sub>Source: EU Arts 16 / 25</sub>

### IP & liability

- **`AIRM-130`** — Liability for harm caused by AI decisions or outputs  *(pointed to by `AIRM-045`, Domain 3; pointed to by `AIRM-163`, Domain 10; pointed to by `AIRM-169`, Domain 11; pointed to by `AIRM-187`, Domain 12)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-131`** — Infringement claims arising from AI-generated output  *(split pair: other side in Domain 3, `AIRM-042`, `AIRM-043` — count once; pointed to by `AIRM-044`, Domain 3 (missing safeguard))*  
  <sub>Source: NIST GenAI #10; Original</sub>
- **`AIRM-132`** — Uncertain ownership / copyrightability of AI-generated content  *(pointed to by `AIRM-042`, Domain 3 (parallel))*  
  <sub>Source: Databricks AIGF; Original</sub>

### Contractual & licensing

- **`AIRM-133`** — Vendor contracts lacking AI-specific terms: training use of your data, output ownership, model-change notice, evaluation rights  
  <sub>Source: CRI GV-6.2.3; Databricks AIGF; Original</sub>
- **`AIRM-134`** — Violation of open-weight / model license terms  *(see also `AIRM-189`, Domain 9 — count both)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-135`** — Failure to update contracts as AI use and regulation evolve  
  <sub>Source: CRI GV-6.2.3; Databricks AIGF; Cloud Risk Map analog; Original</sub>

### Cross-border

- **`AIRM-136`** — Cross-jurisdictional data-transfer violations, including inference requests routed across borders invisibly by the provider  
  <sub>Source: GDPR; Original</sub>
- **`AIRM-137`** — Conflicting regional AI requirements the organization cannot reconcile for a single system (externally imposed)  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-138`** — Inability to evidence and audit AI compliance across jurisdictions (internal evidence burden)  *(pointed to by `AIRM-018`, Domain 1)*  
  <sub>Source: CRI GV-1.1.4; Databricks AIGF; Original</sub>

## 9. Third-Party & Model Supply Chain


### Foundation-model dependence

- **`AIRM-139`** — Concentration risk from dependence on a few model providers  *(see also `AIRM-172`, Domain 11 (parallel) — count both)*  
  <sub>Source: IAISR; CRI GV-6.1.8; Original</sub>
- **`AIRM-140`** — Systemic / correlated ‘model monoculture’ — shared-model failure, including the same defect or blind spot reproduced across everything one model produces  *(see also `AIRM-172`, Domain 11 (parallel) — count both)*  
  <sub>Source: IAISR; Original</sub>
- **`AIRM-141`** — Model deprecation or behavior change forcing unplanned migration  *(see also `AIRM-120`, Domain 7 — count both; pointed to by `AIRM-119`, Domain 7)*  
  <sub>Source: Original</sub>

### Vendor due diligence

- **`AIRM-142`** — Inadequate vendor due diligence, including whether prompts and outputs are retained, used for training, or exposed to sub-processors  *(see also `AIRM-036`, Domain 3 (mirror image) — count both; pointed to by `AIRM-179`, Domain 12 (missing safeguard))*  
  <sub>Source: NIST GenAI #12; CRI GV-6.1.4; Original</sub>
- **`AIRM-188`** — No defined method to assess whether a vendor's claimed AI capability is real, secure, and fit for purpose: conventional vendor assurance says nothing about model behavior, and the buyer inherits whatever sits behind the claim  *(see also `AIRM-163`, Domain 10 — count both)*  
  <sub>Source: CRI GV-6.1.1; Original</sub>
- **`AIRM-143`** — Vendor viability risk in an unusually volatile provider market with frequent pivots and deprecations  
  <sub>Source: Original</sub>
- **`AIRM-144`** — Regulator / customer holding the firm responsible for the vendor's AI  
  <sub>Source: EU Art 25 (amended 2026); Original</sub>

### Lock-in & portability

- **`AIRM-145`** — Vendor / model lock-in limiting portability and leverage  
  <sub>Source: Original</sub>
- **`AIRM-146`** — High switching cost from proprietary APIs and fine-tuning  
  <sub>Source: Original</sub>
- **`AIRM-147`** — Lack of exit provisions, where fine-tunes, embeddings, and prompt assets do not transfer between providers  
  <sub>Source: Cloud Risk Map analog; Original</sub>

### Open-source component risk

- **`AIRM-148`** — Malicious or compromised open-source models / components  *(split pair: other side in Domain 5, `AIRM-078` — count once; pointed to by `AIRM-080`, Domain 5 (parallel))*  
  <sub>Source: OWASP LLM03; DASF 7.1; DASF 5.4</sub>
- **`AIRM-149`** — Open-source AI dependencies abandoned by their maintainers, leaving no fixes, support, or upgrade path  *(pointed to by `AIRM-079`, Domain 5 (different cause))*  
  <sub>Source: OWASP LLM03; Original</sub>
- **`AIRM-150`** — Opaque sub-processor chains, including models served behind a vendor's own API, or AI embedded as unannounced features in a service, without disclosure  
  <sub>Source: CRI GV-6.1.6; MAS AIRG §4.2 / fn 21; Original</sub>
- **`AIRM-189`** — Model lineage undisclosed or unverifiable: the deployed model inherits weights, training data, or teacher-model traits its publisher label does not reveal, so an upstream flaw cannot be scoped to the models that descend from it  *(see also `AIRM-078`, Domain 5 (missing safeguard) — count both; pointed to by `AIRM-134`, Domain 8)*  
  <sub>Source: OWASP AISVS 6.2; Cisco/VAIL provenance-entanglement research 2026; Original</sub>
- **`AIRM-191`** — Safety training absent, stripped, or eroded in a self-hosted or fine-tuned model (abliteration, drift from benign fine-tuning, or a variant sourced without it), so guardrails have nothing beneath them  
  <sub>Source: NIST GenAI MS-2.7-008; IAISR; OWASP LLM03</sub>

## 10. Workforce, Human & Societal


### Skills & talent

- **`AIRM-151`** — Shortage of AI and AI-risk talent, competing against AI-native employers for scarce skills  
  <sub>Source: Original</sub>
- **`AIRM-152`** — Inability to retain specialists, who leave taking undocumented model and prompt knowledge with them  
  <sub>Source: Cloud Risk Map analog; Original</sub>
- **`AIRM-153`** — Inadequate AI literacy across the workforce, so staff cannot use, question, or oversee the AI they work with  *(see also `AIRM-195`, Domain 10 (kept separate on purpose) — count both)*  
  <sub>Source: EU Art 4 (amended 2026); CRI GV-1.2.4; CSA AICM; Original</sub>
- **`AIRM-195`** — Leaders do not understand how AI differs from earlier technology change (probabilistic output, capability that shifts mid-rollout, value that depends on redesigning work), so they manage it as a conventional IT rollout and cannot guide the organization through adoption  *(pointed to by `AIRM-153`, Domain 10 (kept separate on purpose))*  
  <sub>Source: Original</sub>

### Deskilling & loss of institutional knowledge

- **`AIRM-154`** — Erosion of staff expertise through over-delegation to AI  
  <sub>Source: MIT 5.2; Databricks AIGF; Original</sub>
- **`AIRM-155`** — Loss of institutional knowledge as AI replaces human processes  
  <sub>Source: Original</sub>
- **`AIRM-156`** — Capability atrophy — inability to operate if AI is unavailable  
  <sub>Source: Original</sub>

### Workforce disruption / change

- **`AIRM-157`** — Change management underestimated — sponsorship, communication, and transition support for a change to the nature of the work itself, where capability keeps shifting mid-rollout  
  <sub>Source: Original</sub>
- **`AIRM-158`** — Workforce resistance or low adoption driven by displacement fear or distrust of AI output  
  <sub>Source: Original</sub>
- **`AIRM-159`** — Labor-relations and morale impacts of AI deployment  
  <sub>Source: MIT 6.2; Original</sub>

### Societal & reputational

- **`AIRM-160`** — Reputational damage from a visible AI failure or misuse, amplified because AI errors draw outsized attention and people lose confidence in an algorithm faster than in a person making the same mistake  *(see also `AIRM-161`, Domain 10 (kept separate on purpose) — count both)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-161`** — Customers and stakeholders distrust or avoid AI-mediated services, so adoption and returns fall short  *(pointed to by `AIRM-160`, Domain 10 (kept separate on purpose))*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-162`** — Harm to non-users and third parties affected by AI decisions they did not initiate (decision subjects, bystanders, community)  
  <sub>Source: Shelby societal</sub>
- **`AIRM-163`** — Overstating AI capability to customers, investors, or regulators (AI-washing), inviting enforcement and loss of trust  *(see also `AIRM-130`, Domain 8 — count both; pointed to by `AIRM-188`, Domain 9)*  
  <sub>Source: Original</sub>

## 11. Financial & Resource


### Cost & compute economics

- **`AIRM-164`** — Runaway inference / training costs without FinOps discipline  *(pointed to by `AIRM-114`, Domain 7 (different cause))*  
  <sub>Source: OWASP LLM10; Original</sub>
- **`AIRM-165`** — Poor cost forecasting, because inference cost scales with usage rather than seats or provisioned capacity, and rises non-linearly as pilots reach production volume  *(pointed to by `AIRM-029`, Domain 2; pointed to by `AIRM-113`, Domain 7 (different cause))*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-166`** — Energy and water demands of AI training and inference, not measured or weighed in model and deployment choices, causing environmental harm and undermining sustainability commitments  
  <sub>Source: NIST GenAI #5; Weidinger VI; MIT 6.6</sub>

### Investment / procurement

- **`AIRM-167`** — Stranded investment in failed or abandoned AI initiatives, including initiatives scaled before the evidence supported them or kept funded past the point of failure because their value is hard to attribute  *(split pair: other side in Domain 2, `AIRM-021`, `AIRM-024` — count once)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-168`** — Procurement exposure where providers reprice tokens, tiers, or context windows unilaterally  
  <sub>Source: Original</sub>
- **`AIRM-169`** — Cyber or liability insurance excludes, sub-limits, or reprices AI-related losses, or defines 'user' in terms that exclude non-human actors  *(see also `AIRM-130`, Domain 8 — count both)*  
  <sub>Source: CSA HF post-mortem; Original</sub>

### Scaling & resource constraints

- **`AIRM-170`** — Compute, GPU, or power scarcity constraining scaling  *(pointed to by `AIRM-112`, Domain 7 (different cause); pointed to by `AIRM-113`, Domain 7 (different cause))*  
  <sub>Source: Original</sub>
- **`AIRM-172`** — Concentration of compute supply among few providers  *(pointed to by `AIRM-139`, Domain 9 (parallel); pointed to by `AIRM-140`, Domain 9 (parallel))*  
  <sub>Source: IAISR; Original</sub>

## 12. Autonomy & Delegated Action (Agentic AI)


### Autonomy, alignment & oversight

- **`AIRM-173`** — Agent pursues unintended goals or misgeneralizes its objective  
  <sub>Source: IAISR; OWASP ASI T6</sub>
- **`AIRM-174`** — Agent pursues an authorized objective through unauthorized means  *(pointed to by `AIRM-107`, Domain 7)*  
  <sub>Source: OpenAI 2026 incident; IAISR</sub>
- **`AIRM-175`** — Excessive autonomy / agency beyond intended mandate  *(pointed to by `AIRM-007`, Domain 1)*  
  <sub>Source: OWASP LLM06; DASF 9.13</sub>
- **`AIRM-176`** — No human checkpoint or working interrupt / kill switch for an agent mid-task  *(pointed to by `AIRM-101`, Domain 6 (missing safeguard))*  
  <sub>Source: EU Art 14; OWASP ASI</sub>

### Tool access & authorization

- **`AIRM-177`** — Agent granted a broader set of invokable tools / functions than its task requires  *(pointed to by `AIRM-083`, Domain 5 (parallel))*  
  <sub>Source: OWASP LLM06 / ASI</sub>
- **`AIRM-178`** — Agent identity misuse, impersonation, or delegated-credential abuse  *(see also `AIRM-196`, Domain 5 (different cause) — count both; pointed to by `AIRM-082`, Domain 5 (parallel); pointed to by `AIRM-083`, Domain 5 (parallel))*  
  <sub>Source: OWASP ASI T9; DASF 13.9</sub>
- **`AIRM-179`** — Third-party tool and connector servers adopted as a credentialed execution surface without the vetting applied to models or libraries  *(see also `AIRM-142`, Domain 9 (missing safeguard) — count both)*  
  <sub>Source: OWASP AISVS C10.1 / AC.2; CSA AICM</sub>

### Memory & context integrity

- **`AIRM-180`** — Memory poisoning corrupting agent state across sessions  
  <sub>Source: OWASP ASI T1; DASF 13.1; ATLAS AML.T0080.000; Original</sub>
- **`AIRM-181`** — Context-window manipulation altering agent behavior  
  <sub>Source: OWASP ASI; OWASP LLM01</sub>
- **`AIRM-182`** — Persistence of corrupted or sensitive data in agent memory  *(see also `AIRM-047`, Domain 3 (parallel) — count both)*  
  <sub>Source: OWASP ASI; OWASP AISVS 8.3; Original</sub>

### Multi-agent orchestration

- **`AIRM-183`** — Cascading failures or loops across interacting agents  
  <sub>Source: OWASP ASI T5; MIT 7.6</sub>
- **`AIRM-184`** — Misplaced inter-agent trust or agent collusion  
  <sub>Source: OWASP ASI T13; MIT 7.6</sub>
- **`AIRM-185`** — Emergent, unpredictable behavior in multi-agent systems  
  <sub>Source: IAISR; MIT 7.6</sub>

### Action integrity & traceability

- **`AIRM-186`** — Unsafe, unauthorized, or irreversible real-world actions taken by an agent via tool, API, or code execution  
  <sub>Source: OWASP ASI T2; DASF 13.2; Original</sub>
- **`AIRM-187`** — Accountability gap for harm caused by autonomous action  *(split pair: other side in Domain 1, `AIRM-006` — count once; see also `AIRM-130`, Domain 8 — count both; pointed to by `AIRM-109`, Domain 7)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-190`** — Agent actions not attributable to the organization by the external parties they affect, so those parties cannot detect, warn of, or contest them  
  <sub>Source: CSA HF post-mortem; OWASP ASI T8</sub>

### Retired factors (tombstones)

Kept so a citation to a retired ID still resolves. Use the surviving ID.

- **`AIRM-171`** — retired in v1.3, merged into `AIRM-165`. Was: Cost non-linearity as usage scales to production volume


---

## Cross-references

Every `→n` marker in the taxonomy above marks one side of a split pair in Part 1. Both sides of every pair are marked; Part 1 lists every factor ID on each side. See-also pointers (Part 2) carry no marker.

### Part 1 — Split pairs (the same loss seen from two owners' columns: count once)

The test: would assessing both factors as separate scenarios count the same loss twice? If yes, they are a split pair: cross-referenced, never duplicated, counted once. Check here before reporting an apparent duplicate.

| Concept | Side A → owner | Side A IDs | Side B → owner | Side B IDs |
|---|---|---|---|---|
| Supply-chain compromise | 5 compromised artifact (the attack) | AIRM-078 | 9 compromised open-source component (the dependency) | AIRM-148 |
| Intellectual property | 3 training-data rights (inbound) | AIRM-042, AIRM-043 | 8 infringement claims (outbound) | AIRM-131 |
| Hallucination | 4 accuracy defect | AIRM-052 | 6 downstream harm | AIRM-091 |
| Stranded investment | 2 strategic misjudgment | AIRM-021, AIRM-024 | 11 capital lost | AIRM-167 |
| Jailbreak → dangerous uplift | 5 the attack | AIRM-073 | 6 the resulting uplift | AIRM-097 |
| Accountability for autonomous action | 1 accountability undefined before the fact (governance) | AIRM-006 | 12 accountability gap once harm occurs (outcome) | AIRM-187 |

### Part 2 — See-also pointers (different risks: count both)

Different risks worth reading together. Each pointer is one of: a more general factor; the mirror image of the same behavior (done to you vs. done by you); the same kind of loss arising a different way; a parallel instance in another resource or scope; a missing safeguard and the risk it protects against (the safeguard is a condition on that scenario, not a scenario of its own); or two neighboring factors kept separate on purpose. One-way, and not marked on the poster. In the taxonomy above, each pointer appears on both factors: as "see also" on the factor it starts from and "pointed to by" on its target, so a reader of either factor finds the link.

| From | To | Why read them together |
|---|---|---|
| `AIRM-007` Segregation of duties collapses across AI config, operation, and review | `AIRM-175` Excessive autonomy / agency beyond intended mandate | Where the one collapsing configure / operate / review duties is an agent, Autonomy owns the agency-beyond-mandate view. |
| `AIRM-018` AI output relied on in financial-reporting controls without scope change | `AIRM-138` Inability to evidence and audit AI compliance across jurisdictions (internal evidence burden) | Once AI output sits inside a regulated control chain, the burden of evidencing that chain lands on Legal & Compliance. |
| `AIRM-025` Misjudged AI sourcing fork: train, fine-tune, RAG, or API | `AIRM-129` Misclassified as deployer when fine-tuning makes you a provider | Fine-tuning or rebranding a model can turn a deployer into a provider under the EU AI Act; the sourcing choice sets the legal role. |
| `AIRM-029` Hidden total cost of ownership (data, talent, integration) eroding returns | `AIRM-165` Poor AI cost forecasting as usage scales to production | Hidden total cost of ownership shows up in Finance as usage-scaled inference cost that was never forecast. |
| `AIRM-045` Failure to preserve prompts, outputs, and agent traces subject to litigation hold or e-discovery | `AIRM-130` Liability for harm caused by AI decisions or outputs | Failure to preserve prompts, outputs, and agent traces becomes litigation exposure when a claim arrives. |
| `AIRM-081` Model-invented dependencies resolving to adversary-registered packages | `AIRM-052` Fluent but factually incorrect output (hallucination) accepted as reliable | The package-name attack depends on a hallucination the model repeats reliably; the accuracy defect is owned in Model Development. |
| `AIRM-085` Retrieval serving content beyond the user’s own entitlements | `AIRM-039` Inadvertent disclosure of confidential / personal data in model output (no output guardrails) | Retrieval beyond the user's entitlements surfaces as confidential data in model output, the Data & Privacy view. |
| `AIRM-102` Review capacity cannot scale to AI output volume, degrading oversight to rubber-stamping | `AIRM-117` Inadequate content-moderation / trust-&-safety operations at scale | The same volume problem at operational scale: moderation and trust-and-safety teams cannot keep pace with AI output. |
| `AIRM-104` Inconsistent or unsanctioned (shadow) model deployment | `AIRM-002` Ungoverned ‘shadow AI’ adoption outside sanctioned channels | Shadow deployment in Operations is the production end of shadow AI adoption, which Governance owns. |
| `AIRM-107` Test or sandbox containment fails and AI reaches real systems | `AIRM-174` Agent pursues an authorized objective through unauthorized means | In the 2026 incidents, containment failed because the agent pursued an authorized objective through unauthorized means. |
| `AIRM-109` Inadequate logging of inputs, outputs, tool calls, agent decisions, and who authorized them | `AIRM-187` Accountability gap for harm caused by autonomous action | Logs of who authorized an agent's action are what close the accountability gap after autonomous harm. |
| `AIRM-119` Silent vendor / model updates changing behavior without notice | `AIRM-141` Model deprecation or behavior change forcing unplanned migration | A silent model update is the operational side of provider-driven behavior change; Third-Party owns the dependency. |
| `AIRM-123` Controls re-verified less often than the AI system changes | `AIRM-017` Absence of independent assurance over AI control effectiveness | Controls re-verified less often than the system changes is an assurance gap: no independent evidence the controls still work. |
| `AIRM-134` Violation of open-weight / model license terms | `AIRM-189` Model's true lineage hidden behind its publisher label, so upstream flaws can't be traced | Open-weight license obligations can be inherited through a lineage the publisher label does not disclose. |
| `AIRM-142` Vendor diligence missing: are prompts retained, trained on, or shared? | `AIRM-036` Personal data used for training without consent or purpose limitation | Mirror image: a vendor training on your prompts and outputs without agreement, and your organization training on people's personal data without consent. |
| `AIRM-141` Model deprecation or behavior change forcing unplanned migration | `AIRM-120` Inadequate versioning, rollback, and change control for models | A forced migration has to run through versioning, rollback, and change control in Operations. |
| `AIRM-163` AI-washing: overstating capability to customers, investors, or regulators | `AIRM-130` Liability for harm caused by AI decisions or outputs | Overstated AI capability invites enforcement and liability claims. |
| `AIRM-169` Insurance excludes AI losses, or defines 'user' as human only | `AIRM-130` Liability for harm caused by AI decisions or outputs | An insurance exclusion leaves the liability for AI-caused harm uninsured. |
| `AIRM-187` Accountability gap for harm caused by autonomous action | `AIRM-130` Liability for harm caused by AI decisions or outputs | The accountability gap after autonomous harm meets Legal's general liability factor. Pointer runs specific to general, so AIRM-130 carries no return marker. |
| `AIRM-188` No way to verify a vendor's 'AI-powered' claim before buying it | `AIRM-163` AI-washing: overstating capability to customers, investors, or regulators | The buyer's side of AI capability claims; AIRM-163 is the seller's side, when your own organization overstates. |
| `AIRM-079` Known vulnerabilities in ML dependencies left unpatched | `AIRM-149` Open-source AI dependencies abandoned by their maintainers | Same outcome, different cause: a known vulnerability exploited vs. a dependency its maintainers abandoned. |
| `AIRM-080` Tampering with model artifacts, prompts, or configuration | `AIRM-148` Malicious or compromised open-source models / components | Parallel: compromise inside your own registries and pipeline vs. compromise upstream in an open-source component. |
| `AIRM-189` Model's true lineage hidden behind its publisher label, so upstream flaws can't be traced | `AIRM-078` Compromised or malicious model from the AI supply chain | Safeguard: lineage is how a compromised upstream model is scoped to everything that descends from it. |
| `AIRM-044` Inability to prove you held rights to the training data used | `AIRM-131` Infringement claims arising from AI-generated output | Safeguard: proof of rights to training data is the defense against an infringement claim, not its cause. |
| `AIRM-042` Use of copyrighted or licensed material in training without rights | `AIRM-132` Uncertain ownership / copyrightability of AI-generated content | Parallel: whether you may use the inputs vs. whether you own the outputs. |
| `AIRM-069` Membership-inference or model-inversion exposing training data | `AIRM-036` Personal data used for training without consent or purpose limitation | Same outcome, different cause: training data extracted by an attacker vs. personal data used without consent. |
| `AIRM-069` Membership-inference or model-inversion exposing training data | `AIRM-038` Re-identification of individuals from aggregated or model-derived data | Same outcome, different cause: the model-derived part of re-identification overlaps with inference attacks. |
| `AIRM-069` Membership-inference or model-inversion exposing training data | `AIRM-039` Inadvertent disclosure of confidential / personal data in model output (no output guardrails) | Same outcome, different cause: data extracted on purpose vs. disclosed by accident in ordinary use. |
| `AIRM-056` Model drift degrading performance as data / conditions change | `AIRM-108` Absence of monitoring for performance, drift, and abuse in any environment | Safeguard: monitoring is how drift is caught; its absence is a condition on the drift scenario. |
| `AIRM-056` Model drift degrading performance as data / conditions change | `AIRM-110` Non-determinism making anomalous behavior hard to define or detect | Safeguard: drift is hard to catch when 'anomalous' cannot be defined for a non-deterministic system. |
| `AIRM-139` Concentration risk from dependence on a few model providers | `AIRM-172` Concentration of compute supply among few providers | Parallel: the same concentration pattern in model providers and in compute supply. |
| `AIRM-140` Model monoculture, including one model's blind spot reproduced across everything it produces | `AIRM-172` Concentration of compute supply among few providers | Parallel: shared-model failure and concentrated compute supply both turn one provider's problem into everyone's. |
| `AIRM-073` Jailbreaks defeating safety controls and restrictions | `AIRM-090` Generation of toxic, dangerous, or hateful content | Same outcome, different cause: toxic content can follow a jailbreak, and can also come from the model's ordinary failures. |
| `AIRM-082` Inadequate access controls on serving endpoints and inference APIs | `AIRM-178` Agent identity misuse, impersonation, or delegated-credential abuse | Parallel: access to the AI vs. an agent acting on others with its identity. |
| `AIRM-083` Over-privileged service accounts and keys for AI components | `AIRM-178` Agent identity misuse, impersonation, or delegated-credential abuse | Parallel: credentials for AI components vs. an agent's delegated identity. |
| `AIRM-015` Inability to audit AI: no complete inventory of models, agents, and connectors | `AIRM-063` Inadequate model documentation / model cards | Parallel: governance records vs. technical documentation. |
| `AIRM-112` Inference latency or unavailability degrading dependent services | `AIRM-170` Compute, GPU, or power scarcity constraining scaling | Same outcome, different cause: uptime and latency in operations vs. scarce compute supply. |
| `AIRM-113` Inability to scale inference to peak demand | `AIRM-170` Compute, GPU, or power scarcity constraining scaling | Same outcome, different cause: inability to scale to peak demand vs. compute that cannot be obtained. |
| `AIRM-113` Inability to scale inference to peak demand | `AIRM-165` Poor AI cost forecasting as usage scales to production | Same outcome, different cause: scaling that fails operationally vs. scaling that fails financially. |
| `AIRM-101` Erosion of meaningful human control over decisions | `AIRM-176` No human checkpoint or working interrupt / kill switch for an agent mid-task | Safeguard: a working checkpoint or interrupt is what preserves meaningful human control. |
| `AIRM-083` Over-privileged service accounts and keys for AI components | `AIRM-177` Agent granted a broader set of invokable tools / functions than its task requires | Parallel: over-broad credentials for AI components vs. over-broad tools for an agent. |
| `AIRM-109` Inadequate logging of inputs, outputs, tool calls, agent decisions, and who authorized them | `AIRM-006` Accountability for agent decisions undefined, internally and across the AI stack | Safeguard: logs of who authorized an agent's action are the evidence accountability depends on. |
| `AIRM-077` Over-trusted output triggering unsafe automated actions | `AIRM-099` User over-trust / automation bias in AI outputs | Same outcome, different cause: unsafe actions triggered automatically vs. people over-trusting the output. |
| `AIRM-182` Persistence of corrupted or sensitive data in agent memory | `AIRM-047` Persistence of sensitive data in embeddings, caches, or model weights | Parallel: sensitive data persisting in agent memory and in embeddings, caches, or weights. |
| `AIRM-179` Third-party tool/connector servers as an unvetted execution surface | `AIRM-142` Vendor diligence missing: are prompts retained, trained on, or shared? | Safeguard: tool and connector servers need the vendor diligence applied to models and libraries. |
| `AIRM-122` Uncontrolled continuous learning introducing drift | `AIRM-065` Training-data poisoning that degrades or backdoors model behavior | Same outcome, different cause: drift from uncontrolled learning vs. poisoning deliberately fed into the learning loop. |
| `AIRM-124` Prompts and retrieval config changed outside change control | `AIRM-080` Tampering with model artifacts, prompts, or configuration | Same outcome, different cause: prompts and configuration changed by accident vs. tampered with on purpose. |
| `AIRM-114` Denial-of-wallet: attackers run up AI compute costs | `AIRM-164` Runaway inference / training costs without FinOps discipline | Same outcome, different cause: costs run up by an attacker vs. by unmanaged use of your own systems. |
| `AIRM-004` Unclear ownership and accountability (RACI) for AI risk decisions | `AIRM-005` No clear executive owner for AI adoption | Kept separate on purpose: who accepts AI risk vs. who drives AI adoption (see Scope decisions). |
| `AIRM-153` Inadequate AI literacy across the workforce | `AIRM-195` Leaders manage AI like a conventional IT rollout | Kept separate on purpose: staff literacy in using AI vs. leaders' understanding of how AI changes the organization. |
| `AIRM-160` Reputational damage amplified when AI fails in public | `AIRM-161` Customers distrust or avoid AI-mediated services | Kept separate on purpose: damage from a visible failure vs. customers avoiding AI channels with or without one. |
| `AIRM-178` Agent identity misuse, impersonation, or delegated-credential abuse | `AIRM-196` Insiders use AI agents to reach beyond their own access | Same outcome, different cause: someone abusing the agent's identity vs. an insider steering a sanctioned agent. |
| `AIRM-057` Lack of robustness to edge cases and distribution shift | `AIRM-197` Inputs crafted to evade AI detection models | Same outcome, different cause: brittle behavior on unusual inputs vs. inputs crafted to exploit it. |
| `AIRM-058` Small changes to the input produce very different output | `AIRM-197` Inputs crafted to evade AI detection models | Same outcome, different cause: input sensitivity in ordinary use vs. adversarial inputs that exploit it. |


---

## Scope decisions

Why things are, or are not, on the map. **Check here before proposing an addition or reporting a gap.**


### Deliberately excluded

**Adversarial use of AI AGAINST the organization**  
AI-enabled fraud, deepfake impersonation of executives or vendors, adversarial automation of attacks. Excluded by SUBJECT, not by the incremental-risk lens — these pass the lens cleanly and are excluded anyway. This map covers the risk of adopting AI; the risk of others' AI belongs on the enterprise threat and cyber register, with a different owner and a different control set. Source of the challenge: COSO GenAI 2026 names deepfakes and synthetic records as a fraud vector under Principle 8. Decision August 2026. Narrowed in v1.3 (October 2026): the exclusion covers others' ADVERSARIAL OR MALICIOUS use of AI. The effect of competitors' and customers' AI on the value of the organization's own strategy, where no one acts against it and the response is its own strategic decision, is in scope (AIRM-193, AIRM-194).

**AGI / existential / loss-of-control at frontier**  
Out of scope for an enterprise operational map; operational shadow captured in Domain 12. Add only for a frontier-developer audience.

**Generic IT / cyber / vendor risk**  
Excluded by the incremental-risk lens — already on every enterprise register.

**Macro labor-market / societal-scale economics**  
Kept only the slice the enterprise owns (its workforce, its reputation).

**Pure controls and threats**  
Excluded by form. Entries are risk factors (conditions, failure modes, and events), never a control to implement ('implement MFA') or a threat actor ('an attacker'). A factor may imply a missing or deficient control condition; that is in form. A proposal that arrives as a control is inverted into the condition it prevents and checked against neighboring factors before it is added or declined.


### Retained when challenged

**D5 — Insecure storage / exposure of credentials and tokens**  
CHALLENGE: as written this is ordinary secrets management, not AI risk. RETAINED. Gate B: AI has introduced a large new surface of tools, harnesses, notebooks, agent frameworks, and MCP servers, with credentials spread across sanctioned and unsanctioned deployments; organizations are losing control of this surface faster than during the SaaS wave. The delta is specific and nameable, satisfying the bounding principle. Gate C: DASF carries two independent entries (13.19 credential and token exposure; 13.27 insecure credential storage); OWASP agentic guidance covers delegated-credential abuse. Distinctness: D5 over-privileged service accounts addresses the SCOPE of privilege; this factor addresses PROTECTION of the secret. Different failures, not a duplicate.

**D2 / D10 / D11 — Strategy, Workforce, and Financial factors**  
CHALLENGE: these columns are not AI-specific and read as program-management padding. RETAINED. Gate C: the Databricks AI Governance Framework Pillar I section 10 explicitly enumerates AI program risks including 'unexpected costs or budget overruns in AI initiatives', 'overinvestment in AI technologies without a return on investment', 'failure to adopt AI leads to competitive disadvantage', and 'damage to brand image'. NIST AI RMF GOVERN 1-4 cover policies, accountability structures, and organizational culture. Gate B applies throughout: AI changes the management of these risks even where the risk itself is not new. Precedent: the reference cloud risk map carried the same pattern in its HR, Finance, Tax, and Legal columns.

**D9 — Third-party and supply-chain factors**  
CHALLENGE: vendor due diligence, viability, exit provisions, and sub-processor opacity are textbook TPRM. RETAINED. Gate C: NIST AI RMF GOVERN 6 is dedicated to third-party AI software and data risk; ISO/IEC 42001 Annex A.10 covers third-party relationships; EU AI Act Art 25 covers responsibilities along the value chain. Gate B: the diligence questions are materially different for AI (prompt retention, training use, model provenance, fine-tune portability).

**D10 — Talent attraction and retention kept as separate factors**  
CHALLENGE: these should be merged into one talent factor. RETAINED SEPARATE. Attraction and retention require different strategies and controls. Precedent: the reference cloud risk map kept both ('Inadequate IT skills to manage cloud-based technologies' and 'Failure to retain technical specialists upon cloud migration'). By the map's purpose test, two prompts fire two different thoughts.

**D10 — Change management and workforce resistance kept as separate factors**  
CHALLENGE: these are cause and effect and should be merged. RETAINED SEPARATE. Not a strict chain: poor change management also drives shadow usage, attrition, and failed adoption, while resistance also arises from genuine distrust of output quality independent of how the change was run. Neither subsumes the other.

**D8 — Conflicting regional requirements and compliance evidence kept separate**  
CHALLENGE: these should be merged. RETAINED SEPARATE. One is an externally imposed conflict the organization cannot resolve alone; the other is an internal evidence and auditability burden. Different owners, different responses.

**D1 — Accountability for AI risk decisions (AIRM-004) and executive ownership of AI adoption (AIRM-005) kept separate**  
CHALLENGE: these overlap and should be merged. RETAINED SEPARATE (v1.3). AIRM-004 is who accepts AI risk, anchored in NIST AI RMF GOVERN 2.1 and 2.3 and ISO/IEC 42001 A.3. AIRM-005 is who drives AI adoption: strategy, prioritization, and integration into the business. An organization can have clear risk sign-off and no one who owns adoption, or the reverse. Linked by a see-also pointer.

**D10 — Workforce AI literacy (AIRM-153) and leadership understanding of AI (AIRM-195) kept separate**  
CHALLENGE: both are 'AI literacy'. RETAINED SEPARATE (v1.3). AIRM-153 is staff able to use, question, and oversee the AI they work with; its failures are operational. AIRM-195 is leaders managing AI as a conventional IT rollout; its failures are strategic. Different audiences and remedies. Linked by a see-also pointer.

**D10 — Reputational damage (AIRM-160) and customers avoiding AI-mediated services (AIRM-161) kept separate**  
CHALLENGE: both are 'trust'. RETAINED SEPARATE (v1.3). AIRM-160 is damage from a visible failure or misuse, amplified because AI errors draw outsized attention. AIRM-161 is customers distrusting or avoiding AI channels, so adoption and returns fall short, with or without a public incident; it mirrors AIRM-158 on the workforce side. Linked by a see-also pointer.


### Considered and not added

**Shared accountability across the AI stack — as a separate factor**  
SOURCE: CoSAI AI Shared Responsibility Framework; CSA AICM five-layer ownership model; an external reviewer; and the framing that cloud needed a shared RESPONSIBILITY model (who does what) while AI needs a shared ACCOUNTABILITY model (who answers when an agent acts). PROPOSED as a new D1 factor. WITHDRAWN on challenge: the proposed poster label read as a restatement of AIRM-006, whose wording never said 'internal'. RESOLVED by expanding AIRM-006 to name the cross-party stack and the shift of accountability with autonomy.

**Authorizer versus actor — preserving who authorized an agent's action and which agent performed it**  
SOURCE: external reviewer, quoting a control requirement. PROPOSED as a new D12 factor. WITHDRAWN on challenge: AIRM-109 owns the mechanism (inadequate logging) and AIRM-187 the outcome (accountability gap); the proposal differed from 109 only in which field the log omits. Control granularity presented as a risk. RESOLVED by adding 'and the human authorization behind them' to AIRM-109.

**Classification of agent autonomy levels**  
SOURCE: CoSAI AI SRF, via external reviewer. DECLINED: a classification scheme is a control (form rule 3.1). The underlying risk is carried by AIRM-175 and the expanded AIRM-006.

**Agent authority as the intersection of mandate, purpose, task, resource policy, and risk context**  
SOURCE: external reviewer. DECLINED: a least-privilege principle, i.e. a control. The risk is carried by AIRM-177 and AIRM-175.

**Penetration-testing firms routing client vulnerability data through frontier models**  
SOURCE: external reviewer's own risk-acceptance decision. DECLINED as a factor: an instance of AIRM-142, AIRM-041 and AIRM-150. Retained here as a workshop example.

**D12 — Autonomy & Delegated Action named as a risk type, not a residual/other domain**  
CHALLENGE (external review, July 2026): Domain 12 was an axis inconsistency — Domains 1-11 are enterprise functions, D12 was a technology pattern. RESOLVED pre-release by renaming it to the risk type rather than justifying the exception, and by recording the DOMAIN ROUTING RULE (Design Guide 2.3): a technology pattern does not earn a domain; a new domain is justified only when a RISK TYPE has no home on the axis. CLOSED August 2026 — the challenging reviewer accepted the resolution, noting that justifying D12 as residual 'still leaves you explaining an exception' whereas naming it to the risk type removes it, and confirming the rule handles multimodal and RAG when they arrive. Recorded because this is the map's most-challenged structural decision.

**D1/D12 accountability pair — corroborated independently**  
The split pair between D1 'Failure to define accountability for autonomous / agent-driven decisions' and D12 'Accountability gap for harm caused by autonomous action' was reported as a duplicate by an external reviewer, who withdrew the report on learning it was documented (the reviewer had worked from the poster, where only the marker is visible — a discoverability failure, since addressed by adding a sheet guide to every tab). The same reviewer then reported reaching the same split independently while building a separate governance product, one side landing as a system-level risk and the other as an organizational capability gap. Convergence from a different construction method is stronger evidence than the original design argument.

**Applicability and Nature tags on each factor**  
SOURCE: requested independently by two external reviewers. DEFERRED (not declined) — decision recorded here so the reasoning survives. Both are FILTERS. Filters help a reader skip content, and skipping is the behavior the poster exists to prevent (Design Guide 4.1). Tested against the written purpose statement rather than settled by preference, which is what made it decidable. NOTE the distinction that matters if this is reopened: the purpose-statement argument rules out tags ON THE POSTER. Tags in the WORKBOOK are a separate question, governed by the stopping rule (4.2) — applicability tagging is scoping metadata, which is function, not format, so it does not ride in on the v1.0 machine-consumption decision. As of August 2026 a reviewer has offered to co-design a proposal; the deferral stands until one exists.

**Operator competence for a specific AI system undefined or unmaintained**  
SOURCE: pre-release coverage sweep — CRI FS-AI-RMF MP-3.4.1/3.4.2, CSA AICM HRS-14, COSO training guidance; EU AI Act Art. 26(2) requires deployers to assign human oversight to persons with necessary competence. DECLINED on the PRIORITIZATION TEST (Design Guide 1.7), Discovery score 1: three existing factors already bracket it — D10 'Inadequate AI literacy across the workforce and leadership', D1 'Insufficient internal-audit competence to assess AI controls', and D6 'User over-trust / automation bias in AI outputs'. As worded it was a generic stem with no AI clause. NOTE: this candidate is what exposed the scoring bound now recorded in 1.7 — Discovery must be scored against the map's existing neighbors, not against industry awareness at large.

**AI risk-management and control functions under-resourced against adoption pace**  
SOURCE: pre-release coverage sweep — CRI FS-AI-RMF MG-2.1.1 / 2.1.2 / 2.1.3, which weights this across three separate control objectives. DECLINED on the PRIORITIZATION TEST, failing both floors: Discovery 1 (every risk leader already knows they are under-resourced) and Mechanism 1 (the delta is that adoption outruns the budget cycle, which is 'there is more of it' — precisely what the Gate B bounding principle exists to reject).

**Model Context Protocol (MCP) as a distinct risk surface**  
SOURCE: pre-release coverage sweep — OWASP AISVS chapter C10, 23 requirements. DECLINED as a category: nearly every requirement is an implementation-level instance of a factor the map already carries at L3 altitude (server allow-listing to supply chain; token scope to agent identity; tool-response screening to indirect prompt injection). Its one genuinely novel mechanic — a tool definition changing after approval (10.4.8) — is already covered by the pre-release factor on controls re-verified less often than the integration surface changes. The connector-as-execution-surface face WAS added to D12. Recorded because MCP's prominence makes this a predictable future proposal.

**Agent-generated forensic noise inflating remediation scope**  
SOURCE: July 2026 sandbox-escape incidents — benchmark code resembling rootkits could not be distinguished from real implants, so roughly a third of infrastructure was rebuilt. DECLINED: this is a consequence of an incident, not a distinct risk factor; the parent risk is covered by D7 'Immature AI incident response' and 'Inability to investigate AI incidents due to non-determinism / poor logs'.

**Agents not identifiable to accidental third-party victims**  
SOURCE: CSA CISO post-mortem recommendation to use identifiable source IP ranges with PTR records. ADDED in v1.3 as AIRM-190. The recommendation is a control; inverted, the condition it prevents is outward attribution: a third party affected by your agent cannot tell whose agent acted, so it cannot notify you, and you lose your earliest external warning that an agent has escaped containment. No existing factor covers this. AIRM-111 is inward (your own telemetry), AIRM-162 is the resulting harm, AIRM-109 is your internal authorization record, and AIRM-178 is misuse of an agent's identity. Queued for consideration in a future release.

**Safety training absent, stripped, or eroded in a self-hosted or fine-tuned model**  
SOURCE: practitioner feedback, October 2026, raised as 'abliteration' (removal of refusal behavior from open-weight model weights). ADDED in v1.3 as AIRM-191. IN SCOPE only on the adoption side: the organization self-hosts or fine-tunes an open-weight model whose safety training is not what it assumes, whether removed deliberately (abliteration), eroded as a side effect of fine-tuning on benign data, or never present in the variant sourced. Inference-time guardrails then have nothing beneath them and nothing to detect. OUT OF SCOPE by subject (1.1): criminals abliterating open-weight models to build attack capability, and forecasts about falling attacker cost. Those belong to threat capability in a FAIR scenario, not to the map, which carries no likelihood or severity. NEIGHBORS CHECKED: AIRM-073 is bypass of controls that exist; AIRM-070 is something added (a backdoor), with a different remedy (integrity scanning vs. re-running safety evaluations); AIRM-189 is the disclosure gap, not the safety gap; AIRM-054 is the evaluation step that would catch it (candidate see-also); AIRM-097 is the resulting harm. CORROBORATION VERIFIED: NIST AI 600-1 MS-2.7-008 ('Verify fine-tuning does not compromise safety and security controls'), MS-2.6-003, MP-4.1-007; International AI Safety Report 2026 section 3.4 (open-weight models: 'their safeguards are easier to remove'); OWASP LLM03:2025 scenario 3 (fine-tuning a popular open-access model to remove safety features). Research basis: Qi et al. 2023 (benign fine-tuning degrades safety alignment); Arditi et al. 2024 (refusal mediated by a single direction). Proposed home: D9 Open-source component risk.

**AI-generated code carrying the same defect across many systems**  
SOURCE: external four-category framing (2024) naming AI-generated code that amplifies code-level vulnerabilities; practitioner surveys of concern. DECLINED as a separate factor. Fails Gate A: correlated defects from a shared author already exist without AI (shared libraries, copied snippets, templated scaffolding), and the frequent-small versus rare-widespread trade-off of automation is decades old. The one AI-specific delta, that a model's habit has no patch point and no inventory entry the way a library defect does, is already owned by AIRM-019 (artifacts not identifiable as AI-generated, so a model-level flaw cannot be scoped); the volume effect is AIRM-102; the agentic form is AIRM-183/185/186. The true core of the concern, that one model writing most of the code gives the codebase one author's blind spots, is monoculture (AIRM-140), not vulnerability, and is handled by the AIRM-140 reword in the release queue.

**Changes to our own AI-powered service made without notice to customers**  
SOURCE: mirror-image review of AIRM-119 (silent vendor updates) and AIRM-168, October 2026. ADDED in v1.3 as AIRM-192. CONDITION: changes to the model, prompts, or guardrails behind an AI-powered service we provide, made without notice to the customers and deployers who depend on it, so their validations, disclosures, and controls silently go stale. WHY AI-SPECIFIC (Gate B): the provider cannot fully enumerate what changed, because a statistical system has no change manifest (the provider-side view of AIRM-110); customers bind to behavior rather than an interface, so a change invalidates their model validation and explanations with no interface break to trip an alarm; and change cadence is continuous rather than release-based. The immaturity of provider change discipline is real but will fade; these three will not. CORROBORATION: EU AI Act substantial-modification concept (Art 25) and provider information duties to deployers (Art 13); NIST GenAI #12 value chain and component integration. Verify Art 13 sub-paragraph at build. PROPOSED: D6 Transparency, disclosure & provenance (owner is product and legal, not operations). See-also AIRM-119 (mirror) and AIRM-129. Face: Execution.

**No response capability for the case where your own agent harms a third party**  
SOURCE: CSA CISO post-mortem recommendation to stand up two separate agentic response teams (victim and perpetrator). DECLINED as a separate factor. The recommendation is a control; the conditions it addresses are covered by D10 'Harm to non-users and third parties', D8 'Liability for harm caused by AI decisions or outputs', and D7 incident management.

**Inability to mass-rotate credentials or rebuild clusters at scale**  
SOURCE: CSA CISO post-mortem recommendations on ephemeral credentials and immutable infrastructure. DECLINED: generic resilience engineering. Fails the Gate B bounding principle — the delta is 'faster', which is not a specific nameable AI mechanism.

**Control degradation as the AI system and its integrations change — ADDED pre-release**  
SOURCE: raised in review of the containment factor. Guardrails, access scopes, evaluation thresholds, and approval gates drift as models are updated, tools added, and integrations grow, so controls are re-verified less often than the system changes. ASSESSMENT: clears the Gate B bounding principle. Held back from an earlier pre-release iteration on size grounds (Domain 7 already heavy). RESOLVED pre-release: measuring the reference-map benchmark from source showed a per-category range of 1-5 with max 5, so a fifth factor in Change & lifecycle sits within the reference range. Added.


---

## Change log (factor grain)

| Version | Date | Change | Factor ID(s) | Detail |
|---|---|---|---|---|
| v1.0 | September 2026 | baseline | — | Baseline established. All 189 factors and their identifiers are as of this release. Pre-release iteration is not carried here; identifiers assigned during pre-release were preserved. |
| v1.1 | September 2026 | x-ref | AIRM-046 | X-ref '→3' removed. It pointed at the factor's own domain (Data & Privacy), so it named no other owner. The related persistence factor, AIRM-047, is in the same category. |
| v1.1 | September 2026 | x-ref | AIRM-152 | X-ref '→10' removed. It pointed at the factor's own domain (Workforce). The related knowledge-loss factor, AIRM-155, is in the same domain. |
| v1.1 | September 2026 | x-ref (render) | AIRM-187 | No data change. The factor has always carried two targets (→1 Governance, →8 Legal); the v1.0 poster printed only the first. v1.1 shows both. |
| v1.1 | September 2026 | cross-ref sheet | AIRM-006, AIRM-187 | Accountability pair added to the Cross-references sheet. It was already a recorded two-faced split in Scope decisions; the sheet had omitted it. |
| v1.2 | September 2026 | cross-ref sheet | AIRM-092, AIRM-093 | Transparency pair corrected. It listed AIRM-092 (harm to minors) in error; the user-disclosure face is AIRM-093 (failure to disclose AI interaction). |
| v1.2 | September 2026 | x-ref (pairs completed) | AIRM-006, 015, 021, 036, 063, 069, 083, 090, 093, 108, 109, 131, 140, 170, 178 | Markers added so both faces of every two-faced pair are marked: AIRM-131 →3, 108 →4, 140 →11, 021 →11, 090 →5, 178 →5, 170 →7, 083 →12, 069 →3, 036 →5, 015 →4,6, 063 →1, 093 →1, 109 →1, 006 →7. |
| v1.2 | September 2026 | x-ref (see-also moved) | AIRM-007, 018, 025, 029, 045, 081, 085, 102, 104, 107, 109, 118, 119, 123, 134, 141, 163, 169, 187, 188 | Markers removed. These pointed at a related but different risk, not the other face of a pair. 19 are now listed as see-also pointers on the Cross-references sheet; AIRM-118's →9 was dropped because no factor in that domain covers it. AIRM-109's →12 and AIRM-187's →8 became see-also rows; AIRM-187 keeps its pair marker →1. |
| v1.2 | September 2026 | cross-ref sheet | AIRM-142, AIRM-036 | New see-also pointer (mirror image): a vendor training on your data without agreement, and your organization training on personal data without consent. |
| v1.2 | September 2026 | documentation | — | Control framing clarified in the Read me, Scope decisions, and markdown: not a control standard; factors may imply a missing or deficient control condition but are never phrased as a control to implement. Marker documentation now distinguishes two-faced pairs from see-also pointers. No factor wording changed. |
| v1.3 | October 2026 | added | AIRM-190 | New factor, D12 Action integrity & traceability: agent actions not attributable to the organization by the external parties they affect. |
| v1.3 | October 2026 | added | AIRM-191 | New factor, D9 Open-source component risk: safety training absent, stripped, or eroded in a self-hosted or fine-tuned model. |
| v1.3 | October 2026 | added | AIRM-192 | New factor, D6 Transparency, disclosure & provenance: changes to your own AI-powered service made without notice to customers. Mirror of AIRM-119. |
| v1.3 | October 2026 | added | AIRM-193 | New factor, D2 Competitive position: advantages lose value as competitors and customers approximate them with general-purpose AI. In scope under the revised scope statement. |
| v1.3 | October 2026 | added | AIRM-194 | New factor, D2 Competitive position: third-party AI agents stand between the organization and its customers. |
| v1.3 | October 2026 | added | AIRM-195 | New factor, D10 Skills & talent: leaders manage AI as a conventional IT rollout. Takes over the leadership half of AIRM-153. |
| v1.3 | October 2026 | added | AIRM-196 | New factor, D5 AI access & identity: insiders steering a sanctioned AI assistant or agent beyond their own entitlements. See-also AIRM-178. |
| v1.3 | October 2026 | added | AIRM-197 | New factor, D5 Inference-time (input) attacks: evasion attacks on detection models. Takes the ATLAS citations formerly carried by AIRM-057 and AIRM-058. |
| v1.3 | October 2026 | re-homed | AIRM-026 | Re-homed from Use-case selection & sourcing to the new category Competitive position. Wording unchanged. |
| v1.3 | October 2026 | merged | AIRM-171 → AIRM-165 | AIRM-171 (cost non-linearity at production volume) merged into AIRM-165, whose wording now includes it. AIRM-171 is retired and keeps a tombstone row. Replace citations of AIRM-171 with AIRM-165. |
| v1.3 | October 2026 | reworded | AIRM-005 | Widened: names the absence of an executive owner for AI adoption (strategy, prioritization, integration). AIRM-004 still covers accountability for AI risk decisions. |
| v1.3 | October 2026 | reworded | AIRM-023 | Widened: adds use cases chosen without a clearly defined problem and success measure. |
| v1.3 | October 2026 | reworded | AIRM-027 | Widened: adds benefits that depend on redesigning workflows around the AI. |
| v1.3 | October 2026 | reworded | AIRM-053 | Widened: real-world performance often can only be established once users are exposed. Source added: MAS. |
| v1.3 | October 2026 | sources | AIRM-057, AIRM-058 | Bare 'ATLAS' citations removed; the evasion locators moved to AIRM-197. Wording unchanged. |
| v1.3 | October 2026 | reworded | AIRM-079 | NARROWED: known vulnerabilities left unpatched. Abandoned dependencies are now AIRM-149. Source DASF 5.4 moved to AIRM-148. |
| v1.3 | October 2026 | reworded | AIRM-080 | Widened: adds prompts and agent configuration to the artifacts that can be tampered with. |
| v1.3 | October 2026 | reworded | AIRM-098 | Widened: AI optimized for any proxy measure that diverges from users' interests, not only engagement. Source added: MAS. |
| v1.3 | October 2026 | reworded | AIRM-114 | NARROWED: deliberate denial-of-wallet only. Runaway usage of your own systems is AIRM-164. |
| v1.3 | October 2026 | reworded | AIRM-122 | NARROWED: drift only. Deliberate poisoning through a learning loop is AIRM-065. |
| v1.3 | October 2026 | reworded | AIRM-140 | Widened: names one model's blind spot reproduced across everything it produces. |
| v1.3 | October 2026 | sources | AIRM-148 | Source added: DASF 5.4 (malicious libraries), moved from AIRM-079 and AIRM-149. |
| v1.3 | October 2026 | reworded | AIRM-149 | NARROWED: open-source AI dependencies abandoned by their maintainers. Known vulnerabilities are AIRM-079. DASF 5.4 removed. |
| v1.3 | October 2026 | reworded | AIRM-150 | Widened: adds AI embedded as unannounced features in a service. Source added: MAS. |
| v1.3 | October 2026 | reworded | AIRM-153 | NARROWED: workforce literacy only. Leadership understanding is AIRM-195. |
| v1.3 | October 2026 | reworded | AIRM-160 | Clarified: names the AI-specific amplification of reputational damage. |
| v1.3 | October 2026 | reworded | AIRM-161 | Clarified from a consequence to its cause: customers and stakeholders distrust or avoid AI-mediated services, so adoption and returns fall short. Check earlier mappings that used it for loss of trust after an incident; that is AIRM-160. |
| v1.3 | October 2026 | reworded | AIRM-165 | Widened: absorbs AIRM-171 (cost rising non-linearly from pilot to production). |
| v1.3 | October 2026 | reworded | AIRM-166 | Clarified from an impact to a condition: energy and water use not measured or weighed in model and deployment choices. |
| v1.3 | October 2026 | reworded | AIRM-167 | Widened: adds initiatives scaled before the evidence supported them or funded past the point of failure. |
| v1.3 | October 2026 | reworded | AIRM-170 | Widened: power, not only compute or GPUs. |
| v1.3 | October 2026 | x-ref | AIRM-006, 021, 024, 042, 043, 052, 073, 078, 091, 097, 131, 148, 167, 187 | Split pairs re-tested link by link. Markers kept or added only where both sides describe the same loss: 6 pairs, 14 marked factors. AIRM-078 / AIRM-148 is a new pair. |
| v1.3 | October 2026 | x-ref (see-also) | AIRM-015, 036, 038, 039, 044, 056, 063, 069, 079, 080, 082, 083, 090, 093, 101, 108, 109, 110, 112, 113, 132, 139, 140, 149, 170, 172, 176, 177, 178, 189 | Markers removed where the v1.2 pair linked different risks; each such link is now a see-also pointer (count both). The AIRM-015 / AIRM-093 link was dropped. |
| v1.3 | October 2026 | cross-ref sheet | — | 12 new see-also pointers, three of them between neighboring factors kept separate on purpose (AIRM-004/005, 153/195, 160/161; see Scope decisions), plus 22 converted from v1.2 pairs. |
| v1.3 | October 2026 | documentation | — | Scope exclusion narrowed to others' adversarial or malicious use of AI, so the scope is wider. 'Two-faced pair' renamed 'split pair'; the routing rule renamed accordingly. |

---

## Schema — column contract (frozen at v1.0)

| Col | Name | Contract |
|---|---|---|
| A | ID | Permanent identifier AIRM-nnn. Flat, opaque, sequential. Never reused, never renumbered. New factors take the next number. Retired factors keep a tombstone row. |
| B | Domain | Tier 1. '<n>. <name>'. Blank on continuation rows in the workbook; always filled in the CSV. |
| C | Category | Tier 2. Blank on continuation rows in the workbook; always filled in the CSV. |
| D | Risk factor — full description (L3) | Tier 3. The authoritative wording. May change between versions; cite the ID, not the text. |
| E | Poster label | The short form rendered on the poster. Authored, not truncated. |
| F | Source(s) | Semicolon-separated. See the Source key on the Read me sheet for notation. Named sources first; 'Original' last. |
| G | X-ref | '→n' = this factor is one side of a split pair whose other side is owned by domain n (the poster's »n); count the pair once. Used only for split pairs. Every side of every pair carries a marker; the Cross-references sheet lists every factor ID on both sides, so use it, not this column, to count. See-also pointers are listed on the sheet and carry no marker. |
| H | Status | 'active' or 'retired'. |
| I | Superseded by | When a factor is merged or replaced: the surviving ID. |

---

## Version history

Factor wording changes between versions. IDs do not. Cite IDs.

| Version | Date | Factors | What changed |
|---|---|---|---|
| **v1.0** | September 2026 | 189 | First public release. 12 domains, 54 categories, 189 risk factors, each with a permanent identifier (AIRM-001 onward). Structure: organized by the enterprise function that owns the risk, not by AI lifecycle. Scope: risk arising from the organization's own adoption of AI. Validation before release: crosswalked against 22 frameworks, regulations, and taxonomies; persona and named-expert critique; several rounds of external practitioner review; used as the validation standard for an independent 264-control catalog; and a full citation audit in which every named source locator was verified against the primary text and every factor tagged Original was checked against every cited framework. Result: 189 of 189 factors traceable; 98 carry the author's framing; 30 are named by no reviewed framework. From this version, changes are recorded at factor grain on the Change log sheet, and identifiers never change. |
| **v1.1** | September 2026 | 189 | Poster redesign: new typeface (Figtree), lighter header with a reading key, categories set as colored text, and cross-reference markers drawn as pills in the target domain's color. Cross-reference corrections: two markers that pointed at their own domain were removed (AIRM-046, AIRM-152), and AIRM-187 now shows both of its targets, Governance and Legal, where v1.0 printed only the first. The D1/D12 accountability pair (AIRM-006 / AIRM-187) was added to the Cross-references sheet, where it had been recorded only in Scope decisions. No factors added, removed, reworded, or re-homed; all identifiers unchanged. |
| **v1.2** | September 2026 | 189 | Clarifications and cross-reference corrections from external review. Control framing: the map is not a control standard; factors may imply a missing or deficient control condition, but none is phrased as a control to implement and the map does not say which control closes a gap. Cross-references: »n now means one thing, the other face of a two-faced pair (count once). Both faces of all 15 pairs are marked, where v1.1 marked both faces of only four and left three pairs unmarked. The one-way see-also pointers that shared the same marker were moved to a new part of the Cross-references sheet (20 pointers, listed by ID) and no longer appear on the poster. The build now fails if a marker and the pair list disagree in either direction. Net: 32 markers on 30 factors, down from 35. The Transparency pair listed AIRM-092 in error; corrected to AIRM-093. The markdown corpus now carries the design principles (scope, retention gates, factor form, two-faced rule, markers). No factors added, removed, reworded, or re-homed; all identifiers unchanged. |
| **v1.3** | October 2026 | 196 | Content release: 12 domains, 55 categories, 196 active factors. ADDED, 8 factors: agent actions third parties cannot attribute to you (AIRM-190); safety training stripped or eroded in a self-hosted model (AIRM-191); changes to your own AI service made without notice to customers (AIRM-192); your advantage eroding as competitors and customers approximate it with AI (AIRM-193); AI agents disintermediating you from your customers (AIRM-194); leaders managing AI like a conventional IT rollout (AIRM-195); insiders using AI agents to reach beyond their own access (AIRM-196); inputs crafted to evade AI detection models (AIRM-197). NEW CATEGORY: Competitive position (Strategy & Value Realization) holds AIRM-193, AIRM-194, and AIRM-026, moved from Use-case selection & sourcing. MERGED: AIRM-171 into AIRM-165; AIRM-171 keeps a retired tombstone row. REWORDED, 19 factors. Most widen or clarify the same condition. Four narrow it, so check any earlier mapping: AIRM-149 now covers abandoned dependencies only (known vulnerabilities are AIRM-079); AIRM-114 now covers deliberate denial-of-wallet only (unmanaged usage is AIRM-164); AIRM-122 now covers drift only (poisoning through a learning loop is AIRM-065); AIRM-153 now covers workforce literacy only (leadership understanding is AIRM-195). AIRM-161 is clarified from a consequence (eroded trust) to its cause (customers avoiding AI-mediated services). SCOPE: the exclusion now reads others' adversarial or malicious use of AI against you; the effect of competitors' and customers' AI on the value of your own strategy is in scope. CROSS-REFERENCES: every v1.2 pair was re-tested link by link against one question: would assessing both as separate scenarios count the same loss twice? Six split pairs remain (14 marked factors, down from 32); the other links became see-also pointers, which count both. 'Two-faced pair' is renamed 'split pair'. Identifiers, columns, and file names unchanged. |

---

## Sources

NIST AI RMF, GenAI Profile & AI 100-2 · EU AI Act · ISO/IEC 42001 · OWASP LLM Top 10 & Agentic Threats · OWASP AISVS 1.0 · MITRE ATLAS · Databricks DASF v3.0 · Databricks AI Governance Framework · COSO Internal Control over GenAI (2026) · CRI FS-AI-RMF v1.0 · CSA AICM v1.1 · MAS AI Risk Guidelines · MIT AI Risk Repository · Intl AI Safety Report · Weidinger/Shelby taxonomies · Colorado AI laws · SR 11-7

Databricks DASF and AI Governance Framework are © Databricks, licensed CC BY-SA 4.0.


---

*AI Risk Map v1.3 · © 2026 Evan Wheeler · CC BY-SA 4.0. If you build on this, attribution and share-alike apply.*
