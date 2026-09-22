# AI Risk Map — Full Corpus

**Version 1.0 · September 2026 · © 2026 Evan Wheeler · Licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)**

12 domains · 54 categories · 189 risk factors

---

## What this is

A single-page visual reference built to improve the quality of AI risk conversations. Most teams naturally gravitate toward familiar concerns like hallucinations, prompt injection, and bias. But AI risk extends well beyond the usual talking points. The AI Risk Map helps teams quickly widen their perspective, surface blind spots, and identify overlooked risks before moving into deeper analysis.

It is not a risk library or exhaustive catalog. It is a practical tool designed to spark better conversations and uncover overlooked risks.

This file is the machine-readable companion to the poster. It carries every risk factor, plus the scope decisions, source notation, cross-reference reasoning and version history that the poster has no room for.

## What this is NOT

- **Not a scored or ranked risk register.** Position, order, and ID number carry no meaning about likelihood or severity. A rare catastrophic factor sits beside a common minor one.
- **Not a list of well-formed risk statements.** Each entry is a risk *factor* — a condition, failure mode, threat event, or loss event that contributes to risk. In FAIR terms these are not loss-event statements. Scope one properly before using it in analysis.
- **Not exhaustive.** It is a thought-starter. Customize it to your industry, geography, and context.
- **Not a control framework.** It names risks, never controls and never threat actors.
- **Not a replacement for system-specific threat modeling.** It seeds that work; it does not substitute for it.

## Scope boundary — read this before answering coverage questions

**In scope:** risk arising from **your organization's own adoption of AI**.

**Out of scope:** risk arising from **others' use of AI against you** — AI-enabled fraud, deepfake impersonation of executives or vendors, adversarial automation of attacks. That risk is real and growing, but it belongs on the enterprise threat and cyber register, not on an adoption map.

This is a boundary of *subject*, not of degree. AI-enabled phishing is unambiguously amplified by AI and is still out of scope. Do not infer that it is covered.

## Identifiers

Every factor carries a permanent ID (`AIRM-001` onward; 189 active). IDs are flat, opaque and sequential. They encode nothing — not domain, not category, not priority. An ID is stable across versions; **the wording of a factor is not**. Cite the ID, not the sentence.

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
   "Cross-references" section. Many risks have two legitimate faces
   owned by different functions and are split on purpose.
6. Your job is to widen my thinking, not narrow it. When I describe
   a system or a decision, surface the factors I have not considered
   yet, including ones from domains outside my own function.
```

**Questions this file answers well:**

- "We're deploying a customer-facing agent. Walk me through the factors we should discuss, domain by domain."
- "Is *X* covered? If not, was it deliberately excluded, and why?"
- "Show me everything Legal owns. Now everything Finance owns."
- "Which factors have two faces I might double-count?"
- "We just had this incident. Which factors does it touch?"
- "Which of these factors would a security team typically miss?"

**Questions it cannot answer:** anything about likelihood, cost, severity, maturity, or control effectiveness. That data is not here by design.


---

## The taxonomy


## 1. AI Governance & Accountability


### Governance & oversight

- **`AIRM-001`** — Inadequate executive/board oversight of AI adoption and risk  
  <sub>Source: NIST Govern; ISO A.2</sub>
- **`AIRM-002`** — Ungoverned ‘shadow AI’ adoption outside sanctioned channels  
  <sub>Source: NIST Govern; CRI GV-1.6.3; COSO GenAI 2026; Original</sub>
- **`AIRM-003`** — Absence of an AI governance body or charter with a clear mandate  
  <sub>Source: ISO A.3</sub>

### Roles & accountability

- **`AIRM-004`** — Unclear ownership and accountability (RACI) for AI risk decisions  
  <sub>Source: NIST Govern; ISO A.3</sub>
- **`AIRM-005`** — Diffusion of responsibility, as AI spans data science, security, legal, and business owners with no established convention for who decides  
  <sub>Source: Original</sub>
- **`AIRM-006`** — Failure to define accountability for autonomous / agent-driven decisions — internally, and across the AI stack of model provider, platform, developer, and deployer, where the allocation shifts as autonomy increases  *(also has a face in Domain 12 — see Cross-references)*  
  <sub>Source: EU Art 14; EU Art 25 (amended 2026); CSA AICM; CoSAI AI SRF</sub>
- **`AIRM-007`** — Segregation of duties collapses where the same person or agent configures the AI, operates it, and reviews its output  *(also has a face in Domain 12 — see Cross-references)*  
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

- **`AIRM-015`** — Inability to audit AI due to a missing or incomplete inventory of models, agents, and connectors, and their lineage  
  <sub>Source: ISO A.4; NIST Govern; CRI GV-1.6.1</sub>
- **`AIRM-016`** — Insufficient internal-audit competence to assess AI controls  
  <sub>Source: Original</sub>
- **`AIRM-017`** — Absence of independent assurance over AI control effectiveness  
  <sub>Source: CRI GV-1.5.4; Original</sub>
- **`AIRM-018`** — AI output relied upon as evidence in financial-reporting or other regulated control chains without recognizing the expansion of assurance scope  *(also has a face in Domain 8 — see Cross-references)*  
  <sub>Source: COSO GenAI 2026 p.13</sub>
- **`AIRM-019`** — No reliable way to identify which artifacts, code, or analyses were AI-generated, so a systemic model or prompt flaw cannot be scoped or remediated after the fact  
  <sub>Source: OWASP AISVS AC.9 / AC.10; COSO GenAI 2026 (AI bill of materials)</sub>

## 2. Strategy & Value Realization


### AI strategy & roadmap

- **`AIRM-020`** — Lack of a coherent AI strategy aligned to objectives and risk appetite  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-021`** — AI adoption driven by hype rather than demonstrated business value  
  <sub>Source: Original</sub>
- **`AIRM-022`** — Inability to adapt the roadmap as foundation-model capabilities shift  
  <sub>Source: Original</sub>

### Use-case selection & sourcing

- **`AIRM-023`** — Selection of use cases without weighing incremental risk against benefit  
  <sub>Source: CRI MP-3.2.1; Original</sub>
- **`AIRM-024`** — ‘Pilot purgatory’ — pilots stalling on data readiness, evaluation difficulty, or inability to demonstrate value  
  <sub>Source: Original</sub>
- **`AIRM-025`** — Misjudged AI sourcing fork — train, fine-tune, retrieval-augment, or call an API — each carrying a different risk and obligation profile  *(also has a face in Domain 8 — see Cross-references)*  
  <sub>Source: Original</sub>
- **`AIRM-026`** — Failure to weigh the competitive risk of not adopting AI (inaction)  
  <sub>Source: Databricks AIGF; Cloud Risk Map analog; Original</sub>

### Value measurement / ROI

- **`AIRM-027`** — Unrealistic ROI expectations, where AI benefits are diffuse and hard to attribute to the system itself  
  <sub>Source: Original</sub>
- **`AIRM-028`** — Inability to attribute value actually delivered by AI investments  
  <sub>Source: Original</sub>
- **`AIRM-029`** — Hidden total cost of ownership (data, talent, integration) eroding returns  *(also has a face in Domain 11 — see Cross-references)*  
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

- **`AIRM-036`** — Personal data used for training without consent or purpose limitation  
  <sub>Source: EU Art 10 (amended 2026); NIST GenAI #4</sub>
- **`AIRM-037`** — Inability to honor data-subject rights once data is in a model  
  <sub>Source: GDPR; DASF 1.8; Original</sub>
- **`AIRM-038`** — Re-identification of individuals from aggregated or model-derived data  
  <sub>Source: MIT 2.1</sub>
- **`AIRM-039`** — Inadvertent disclosure of confidential / personal data in model output (no output guardrails)  
  <sub>Source: OWASP LLM02; DASF 10.6</sub>
- **`AIRM-040`** — Sensitive or regulated data used in AI without classification, so handling and access controls are not applied  
  <sub>Source: Databricks AIGF; ISO A.7</sub>
- **`AIRM-041`** — Users pasting confidential or client data into a sanctioned AI tool, moving data outside its control boundary despite upstream access controls working  
  <sub>Source: OWASP AISVS AC.3; COSO GenAI 2026; Original</sub>

### Training-data rights & IP

- **`AIRM-042`** — Use of copyrighted or licensed material in training without rights  *(also has a face in Domain 8 — see Cross-references)*  
  <sub>Source: NIST GenAI #10; EU Art 53(1)(c) (amended 2026)</sub>
- **`AIRM-043`** — Contamination of datasets with third-party IP or trade secrets  
  <sub>Source: Original</sub>
- **`AIRM-044`** — Inability to prove the organization held the rights to the training data it used  
  <sub>Source: OWASP AISVS 1.1.2; DASF 1.8; Original</sub>

### Retention & disposal

- **`AIRM-045`** — Failure to preserve prompts, outputs, and agent traces subject to litigation hold or e-discovery  *(also has a face in Domain 8 — see Cross-references)*  
  <sub>Source: Cloud Risk Map analog; Original</sub>
- **`AIRM-046`** — Inadequate retention / disposal, where deletion from source systems does not remove data already absorbed into models, embeddings, or caches  *(also has a face in Domain 3 — see Cross-references)*  
  <sub>Source: DASF 1.8; ISO A.7; Original</sub>
- **`AIRM-047`** — Persistence of sensitive data in embeddings, caches, or model weights  
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

- **`AIRM-052`** — Fluent but factually incorrect output (hallucination) accepted as reliable  *(also has a face in Domain 6 — see Cross-references)*  
  <sub>Source: NIST GenAI #2; DASF 9.8</sub>
- **`AIRM-053`** — Validation/evaluation data not representative of real-world use  
  <sub>Source: DASF 6.2</sub>
- **`AIRM-054`** — Skipped or insufficient pre-deployment red-teaming / safety evaluation  
  <sub>Source: EU Art 9; NIST Measure</sub>
- **`AIRM-055`** — Absence of independent model validation / effective challenge  
  <sub>Source: SR 11-7; CRI MS-2.5.1; Original</sub>

### Robustness & drift

- **`AIRM-056`** — Model drift degrading performance as data / conditions change  *(also has a face in Domain 7 — see Cross-references)*  
  <sub>Source: DASF 5.2</sub>
- **`AIRM-057`** — Lack of robustness to edge cases and distribution shift  
  <sub>Source: NIST Measure; ATLAS</sub>
- **`AIRM-058`** — Small changes to the input produce very different output  
  <sub>Source: ATLAS; Original</sub>

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
- **`AIRM-063`** — Inadequate model documentation / model cards  
  <sub>Source: EU Art 11 (amended 2026); NIST Map</sub>
- **`AIRM-064`** — Loss of traceability between model versions, data, and results  
  <sub>Source: DASF 4.1</sub>

## 5. Security & Adversarial Threats


### Data & pipeline attacks

- **`AIRM-065`** — Training-data poisoning that degrades or backdoors model behavior  
  <sub>Source: DASF 3.1; OWASP LLM04; ATLAS AML.T0020</sub>
- **`AIRM-066`** — Tampering with RAG / knowledge-base sources consumed at inference  
  <sub>Source: OWASP LLM08; DASF 9.9</sub>
- **`AIRM-067`** — Label-flipping or adversarial dataset partitioning to skew outputs  
  <sub>Source: DASF 3.3 / 2.4</sub>

### Model attacks

- **`AIRM-068`** — Model extraction / theft via inference-API querying  
  <sub>Source: DASF 8.2; ATLAS AML.T0024.002</sub>
- **`AIRM-069`** — Membership-inference or model-inversion exposing training data  
  <sub>Source: DASF 9.2 / 9.5; NIST GenAI #4</sub>
- **`AIRM-070`** — Backdoored / trojaned pre-trained model from a public hub  
  <sub>Source: DASF 7.1</sub>

### Inference-time (input) attacks

- **`AIRM-071`** — Direct prompt injection altering behavior or bypassing guardrails  
  <sub>Source: OWASP LLM01; DASF 9.1</sub>
- **`AIRM-072`** — Indirect / cross-domain prompt injection via retrieved content  
  <sub>Source: OWASP LLM01; DASF 9.1 / 9.9</sub>
- **`AIRM-073`** — Jailbreaks defeating safety controls and restrictions  *(also has a face in Domain 6 — see Cross-references)*  
  <sub>Source: OWASP LLM01; DASF 9.12</sub>
- **`AIRM-074`** — System-prompt leakage exposing operational instructions  
  <sub>Source: OWASP LLM07</sub>

### Output & integration security

- **`AIRM-075`** — Unsanitized output reaching downstream interpreters (code exec / XSS / SQLi)  
  <sub>Source: OWASP LLM05</sub>
- **`AIRM-076`** — Interception or manipulation of the inference output stream  
  <sub>Source: DASF 10.2</sub>
- **`AIRM-077`** — Over-trusted output triggering unsafe automated actions  
  <sub>Source: OWASP LLM05 / LLM06</sub>

### Supply-chain & artifact integrity

- **`AIRM-078`** — Compromised or malicious model / component from the AI supply chain  *(also has a face in Domain 9 — see Cross-references)*  
  <sub>Source: OWASP LLM03; NIST GenAI #12</sub>
- **`AIRM-079`** — Vulnerable or unmaintained ML dependencies and libraries  
  <sub>Source: DASF 5.4; OWASP LLM03</sub>
- **`AIRM-080`** — Tampering with model artifacts in registries or during deployment  
  <sub>Source: DASF 7.3; ATLAS AML.T0010.004; Original</sub>
- **`AIRM-081`** — Model-invented package, image, or endpoint names that resolve to adversary-registered artifacts, because the same hallucination recurs across users and model families  *(also has a face in Domain 4 — see Cross-references)*  
  <sub>Source: OWASP AISVS AC.13</sub>

### AI access & identity

- **`AIRM-082`** — Inadequate access controls on serving endpoints and inference APIs  *(also has a face in Domain 12 — see Cross-references)*  
  <sub>Source: DASF 9.11</sub>
- **`AIRM-083`** — Over-privileged service accounts and keys for AI platform components (distinct from an agent's tool scope)  
  <sub>Source: DASF 1.1; Original</sub>
- **`AIRM-084`** — Insecure storage / exposure of credentials and tokens, as AI tool, harness, and agent-framework sprawl outpaces credential governance  
  <sub>Source: DASF 13.19 / 13.27</sub>
- **`AIRM-085`** — Retrieval and RAG pipelines serving content beyond the requesting user’s own entitlements, because authorization is applied when the index is built rather than when it is queried  *(also has a face in Domain 3 — see Cross-references)*  
  <sub>Source: OWASP AISVS 5.2.2</sub>

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

- **`AIRM-090`** — Generation of toxic, dangerous, or hateful content  
  <sub>Source: NIST GenAI #3; Weidinger I</sub>
- **`AIRM-091`** — Harmful, misleading, or defamatory output driving decisions  *(also has a face in Domain 4 — see Cross-references)*  
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

### Misuse & dual-use

- **`AIRM-096`** — Misuse of AI for disinformation, fraud, or social engineering  
  <sub>Source: NIST GenAI; Weidinger IV; IAISR</sub>
- **`AIRM-097`** — Dangerous-capability uplift: the model gives meaningful help toward chemical, biological, radiological, nuclear, or cyber attack capability  
  <sub>Source: NIST GenAI #1; Weidinger IV; IAISR</sub>
- **`AIRM-098`** — Engagement-optimized AI driving addiction, polarization, or harm  
  <sub>Source: Shelby societal; Original</sub>

### Human agency & over-reliance

- **`AIRM-099`** — User over-trust / automation bias in AI outputs  
  <sub>Source: NIST GenAI #7; Weidinger V</sub>
- **`AIRM-100`** — Anthropomorphism and emotional dependence on conversational AI  
  <sub>Source: Weidinger V; Colorado HB 26-1263</sub>
- **`AIRM-101`** — Erosion of meaningful human control over decisions  *(also has a face in Domain 12 — see Cross-references)*  
  <sub>Source: EU Art 14; MIT 5.2</sub>
- **`AIRM-102`** — Human review, approval, and triage capacity cannot scale to the volume AI produces — code, alerts, content, decisions — so oversight gates degrade into rubber-stamping while still appearing effective  *(also has a face in Domain 7 — see Cross-references)*  
  <sub>Source: COSO GenAI 2026; OWASP AISVS AC.4; CRI MP-3.5.4</sub>

## 7. Operations & Resilience


### MLOps & deployment

- **`AIRM-103`** — Immature MLOps / fragile deployment pipelines  
  <sub>Source: DASF 11.1; Original</sub>
- **`AIRM-104`** — Inconsistent or unsanctioned (shadow) model deployment  *(also has a face in Domain 1 — see Cross-references)*  
  <sub>Source: DASF 8.3; Original</sub>
- **`AIRM-105`** — Inadequate environment and configuration management across model versions, dependency pinning, and accelerator configuration, undermining reproducibility  
  <sub>Source: DASF 12.5</sub>
- **`AIRM-106`** — Training-serving skew: features or input data differ between training and production, degrading live performance  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-107`** — Containment of an AI test, evaluation, or development environment fails — unverified, misconfigured, defeated, or degraded over time — allowing the system to reach production or third-party systems  *(also has a face in Domain 12 — see Cross-references)*  
  <sub>Source: OpenAI/Anthropic 2026 incidents</sub>

### Monitoring & observability

- **`AIRM-108`** — Absence of monitoring for performance, drift, and abuse in any environment — including evaluation, test, and sandbox environments assumed to be contained  
  <sub>Source: DASF 10.1; NIST Manage; CSA HF post-mortem</sub>
- **`AIRM-109`** — Inadequate logging / audit of inputs, outputs, tool calls, agent decision paths, and the human authorization behind them  *(also has a face in Domain 12 — see Cross-references)*  
  <sub>Source: EU Art 12; DASF 10.1</sub>
- **`AIRM-110`** — Inability to detect anomalous or degraded behavior, where non-determinism makes 'anomalous' hard to define and baseline  
  <sub>Source: DASF 10.1; Original</sub>
- **`AIRM-111`** — Sanctioned agent activity indistinguishable from agentic attack in telemetry  
  <sub>Source: CSA HF post-mortem</sub>

### Availability & scalability

- **`AIRM-112`** — Inference latency or unavailability degrading dependent services  *(also has a face in Domain 11 — see Cross-references)*  
  <sub>Source: Databricks AIGF; CSA AICM; Original</sub>
- **`AIRM-113`** — Inability to scale inference to peak demand  
  <sub>Source: Original</sub>
- **`AIRM-114`** — Unbounded resource consumption / denial-of-wallet from AI workloads  
  <sub>Source: OWASP LLM10</sub>

### Incident management

- **`AIRM-115`** — Immature AI incident response and escalation processes  
  <sub>Source: NIST Manage; CRI GV-4.3.2; DASF 12.3; Original</sub>
- **`AIRM-116`** — Inability to investigate AI incidents due to non-determinism / poor logs  
  <sub>Source: DASF 12.3; CRI MS-2.4.4; Original</sub>
- **`AIRM-117`** — Inadequate content-moderation / trust-&-safety operations at scale  
  <sub>Source: Colorado HB 26-1263; Original</sub>
- **`AIRM-118`** — Safety guardrails on models relied on for defense refusing to assist incident response, blocking analysis of attack data  *(also has a face in Domain 9 — see Cross-references)*  
  <sub>Source: CSA HF post-mortem</sub>

### Change & lifecycle management

- **`AIRM-119`** — Silent vendor / model updates changing behavior without notice  *(also has a face in Domain 9 — see Cross-references)*  
  <sub>Source: COSO GenAI 2026; OWASP AISVS 3.2.3; Original</sub>
- **`AIRM-120`** — Inadequate versioning, rollback, and change control for models  
  <sub>Source: DASF 8.3; CRI MG-4.1.4; Original</sub>
- **`AIRM-121`** — Unmanaged model decommissioning / sunset leaving orphaned dependencies  
  <sub>Source: CRI GV-1.7.1; CRI MG-2.4.2; Original</sub>
- **`AIRM-122`** — Uncontrolled continuous / online learning introducing drift or poisoning  
  <sub>Source: DASF 5.2; Original</sub>
- **`AIRM-123`** — Guardrails, access scopes, and approval gates re-verified less often than the AI system's capability and integration surface changes  *(also has a face in Domain 1 — see Cross-references)*  
  <sub>Source: 2026 sandbox-escape incidents; Original</sub>
- **`AIRM-124`** — Prompts, system prompts, and retrieval configuration changed outside change control, though they determine system behavior as directly as code  
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
- **`AIRM-129`** — Misclassifying the organization's regulatory role (deployer vs. provider), missing obligations triggered by fine-tuning or rebranding a model  
  <sub>Source: EU Arts 16 / 25</sub>

### IP & liability

- **`AIRM-130`** — Liability for harm caused by AI decisions or outputs  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-131`** — Infringement claims arising from AI-generated output  
  <sub>Source: NIST GenAI #10; Original</sub>
- **`AIRM-132`** — Uncertain ownership / copyrightability of AI-generated content  
  <sub>Source: Databricks AIGF; Original</sub>

### Contractual & licensing

- **`AIRM-133`** — Vendor contracts lacking AI-specific terms: training use of your data, output ownership, model-change notice, evaluation rights  
  <sub>Source: CRI GV-6.2.3; Databricks AIGF; Original</sub>
- **`AIRM-134`** — Violation of open-weight / model license terms  *(also has a face in Domain 9 — see Cross-references)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-135`** — Failure to update contracts as AI use and regulation evolve  
  <sub>Source: CRI GV-6.2.3; Databricks AIGF; Cloud Risk Map analog; Original</sub>

### Cross-border

- **`AIRM-136`** — Cross-jurisdictional data-transfer violations, including inference requests routed across borders invisibly by the provider  
  <sub>Source: GDPR; Original</sub>
- **`AIRM-137`** — Conflicting regional AI requirements the organization cannot reconcile for a single system (externally imposed)  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-138`** — Inability to evidence and audit AI compliance across jurisdictions (internal evidence burden)  
  <sub>Source: CRI GV-1.1.4; Databricks AIGF; Original</sub>

## 9. Third-Party & Model Supply Chain


### Foundation-model dependence

- **`AIRM-139`** — Concentration risk from dependence on a few model providers  
  <sub>Source: IAISR; CRI GV-6.1.8; Original</sub>
- **`AIRM-140`** — Systemic / correlated ‘model monoculture’ — shared-model failure  
  <sub>Source: IAISR; Original</sub>
- **`AIRM-141`** — Model deprecation or behavior change forcing unplanned migration  *(also has a face in Domain 7 — see Cross-references)*  
  <sub>Source: Original</sub>

### Vendor due diligence

- **`AIRM-142`** — Inadequate vendor due diligence, including whether prompts and outputs are retained, used for training, or exposed to sub-processors  
  <sub>Source: NIST GenAI #12; CRI GV-6.1.4; Original</sub>
- **`AIRM-188`** — No defined method to assess whether a vendor's claimed AI capability is real, secure, and fit for purpose: conventional vendor assurance says nothing about model behavior, and the buyer inherits whatever sits behind the claim  *(also has a face in Domain 10 — see Cross-references)*  
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

- **`AIRM-148`** — Malicious or compromised open-source models / components  
  <sub>Source: OWASP LLM03; DASF 7.1</sub>
- **`AIRM-149`** — Unmaintained or vulnerable open-source AI dependencies  
  <sub>Source: OWASP LLM03; DASF 5.4</sub>
- **`AIRM-150`** — Opaque sub-processor chains, including models served behind a vendor's own API without disclosure  
  <sub>Source: CRI GV-6.1.6; Original</sub>
- **`AIRM-189`** — Model lineage undisclosed or unverifiable: the deployed model inherits weights, training data, or teacher-model traits its publisher label does not reveal, so an upstream flaw cannot be scoped to the models that descend from it  *(also has a face in Domain 5 — see Cross-references)*  
  <sub>Source: OWASP AISVS 6.2; Cisco/VAIL provenance-entanglement research 2026; Original</sub>

## 10. Workforce, Human & Societal


### Skills & talent

- **`AIRM-151`** — Shortage of AI and AI-risk talent, competing against AI-native employers for scarce skills  
  <sub>Source: Original</sub>
- **`AIRM-152`** — Inability to retain specialists, who leave taking undocumented model and prompt knowledge with them  *(also has a face in Domain 10 — see Cross-references)*  
  <sub>Source: Cloud Risk Map analog; Original</sub>
- **`AIRM-153`** — Inadequate AI literacy across the workforce and leadership  
  <sub>Source: EU Art 4 (amended 2026); CRI GV-1.2.4; CSA AICM; Original</sub>

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

- **`AIRM-160`** — Reputational damage from a visible AI failure or misuse  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-161`** — Erosion of customer / stakeholder trust in AI-mediated services  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-162`** — Harm to non-users and third parties affected by AI decisions they did not initiate (decision subjects, bystanders, community)  
  <sub>Source: Shelby societal</sub>
- **`AIRM-163`** — Overstating AI capability to customers, investors, or regulators (AI-washing), inviting enforcement and loss of trust  *(also has a face in Domain 8 — see Cross-references)*  
  <sub>Source: Original</sub>

## 11. Financial & Resource


### Cost & compute economics

- **`AIRM-164`** — Runaway inference / training costs without FinOps discipline  
  <sub>Source: OWASP LLM10; Original</sub>
- **`AIRM-165`** — Poor cost forecasting, because inference cost scales with usage rather than seats or provisioned capacity  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-166`** — Environmental / energy footprint of training and inference  
  <sub>Source: NIST GenAI #5; Weidinger VI; MIT 6.6</sub>

### Investment / procurement

- **`AIRM-167`** — Stranded investment in failed or abandoned AI initiatives  *(also has a face in Domain 2 — see Cross-references)*  
  <sub>Source: Databricks AIGF; Original</sub>
- **`AIRM-168`** — Procurement exposure where providers reprice tokens, tiers, or context windows unilaterally  
  <sub>Source: Original</sub>
- **`AIRM-169`** — Cyber or liability insurance excludes, sub-limits, or reprices AI-related losses, or defines 'user' in terms that exclude non-human actors  *(also has a face in Domain 8 — see Cross-references)*  
  <sub>Source: CSA HF post-mortem; Original</sub>

### Scaling & resource constraints

- **`AIRM-170`** — Compute / GPU scarcity constraining scaling  
  <sub>Source: Original</sub>
- **`AIRM-171`** — Cost non-linearity as usage scales to production volume  
  <sub>Source: Original</sub>
- **`AIRM-172`** — Concentration of compute supply among few providers  *(also has a face in Domain 9 — see Cross-references)*  
  <sub>Source: IAISR; Original</sub>

## 12. Autonomy & Delegated Action (Agentic AI)


### Autonomy, alignment & oversight

- **`AIRM-173`** — Agent pursues unintended goals or misgeneralizes its objective  
  <sub>Source: IAISR; OWASP ASI T6</sub>
- **`AIRM-174`** — Agent pursues an authorized objective through unauthorized means  
  <sub>Source: OpenAI 2026 incident; IAISR</sub>
- **`AIRM-175`** — Excessive autonomy / agency beyond intended mandate  
  <sub>Source: OWASP LLM06; DASF 9.13</sub>
- **`AIRM-176`** — No human checkpoint or working interrupt / kill switch for an agent mid-task  *(also has a face in Domain 6 — see Cross-references)*  
  <sub>Source: EU Art 14; OWASP ASI</sub>

### Tool access & authorization

- **`AIRM-177`** — Agent granted a broader set of invokable tools / functions than its task requires  *(also has a face in Domain 5 — see Cross-references)*  
  <sub>Source: OWASP LLM06 / ASI</sub>
- **`AIRM-178`** — Agent identity misuse, impersonation, or delegated-credential abuse  
  <sub>Source: OWASP ASI T9; DASF 13.9</sub>
- **`AIRM-179`** — Third-party tool and connector servers adopted as a credentialed execution surface without the vetting applied to models or libraries  
  <sub>Source: OWASP AISVS C10.1 / AC.2; CSA AICM</sub>

### Memory & context integrity

- **`AIRM-180`** — Memory poisoning corrupting agent state across sessions  
  <sub>Source: OWASP ASI T1; DASF 13.1; ATLAS AML.T0080.000; Original</sub>
- **`AIRM-181`** — Context-window manipulation altering agent behavior  
  <sub>Source: OWASP ASI; OWASP LLM01</sub>
- **`AIRM-182`** — Persistence of corrupted or sensitive data in agent memory  
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
- **`AIRM-187`** — Accountability gap for harm caused by autonomous action  *(also has a face in Domain 1,8 — see Cross-references)*  
  <sub>Source: Databricks AIGF; Original</sub>


---

## Cross-references — the two-faced splits

Many AI risks have an **attack face** and a **condition face**, owned by different functions. The attack face routes to Security or Autonomy; the condition face to the function that owns it. They are cross-referenced, never duplicated. Check here before reporting an apparent duplicate.

| Concept | Face A → owner | Face A IDs | Face B → owner | Face B IDs |
|---|---|---|---|---|
| Supply chain | 5 artifact integrity | AIRM-078, AIRM-079, AIRM-080 | 9 dependence / commercial / lineage | AIRM-148, AIRM-149, AIRM-189 |
| Intellectual property | 3 training-data rights (inbound) | AIRM-042, AIRM-043, AIRM-044 | 8 infringement / ownership (outbound) | AIRM-131, AIRM-132 |
| Privacy | 5 attack / leakage | AIRM-069 | 3 consent / compliance | AIRM-036, AIRM-038, AIRM-039 |
| Hallucination | 4 accuracy defect | AIRM-052 | 6 downstream harm | AIRM-091 |
| Model drift | 4 the phenomenon | AIRM-056 | 7 detection / monitoring | AIRM-108, AIRM-110 |
| Concentration | 9 model monoculture | AIRM-139, AIRM-140 | 11 compute / resource scaling | AIRM-172 |
| Stranded investment | 2 strategic misjudgment | AIRM-021, AIRM-024 | 11 capital lost | AIRM-167 |
| Jailbreak → harm | 5 the attack | AIRM-073 | 6 the resulting harm | AIRM-090, AIRM-097 |
| Identity & access | 5 access TO the AI | AIRM-082, AIRM-083 | 12 agent identity acting ON others | AIRM-178 |
| Transparency | 1 governance records | AIRM-015 | 4 technical docs / 6 user disclosure | AIRM-063, AIRM-092 |
| Availability / scaling | 7 uptime / performance | AIRM-112, AIRM-113 | 11 compute affordability / supply | AIRM-170, AIRM-171 |
| Human oversight | 6 humans have lost meaningful control (outcome) | AIRM-101 | 12 no checkpoint or interrupt mechanism exists (capability) | AIRM-176 |
| Privilege scope | 5 credentials / keys for AI components | AIRM-083 | 12 breadth of tools an agent may invoke | AIRM-177 |
| Audit & traceability | 7 logging of inputs, outputs, agent actions | AIRM-109 | 1 accountability for who owns the decision | AIRM-006 |


---

## Scope decisions

Why things are, or are not, on the map. **Check here before proposing an addition or reporting a gap.**


### Deliberately excluded

**Adversarial use of AI AGAINST the organization**  
AI-enabled fraud, deepfake impersonation of executives or vendors, adversarial automation of attacks. Excluded by SUBJECT, not by the incremental-risk lens — these pass the lens cleanly and are excluded anyway. This map covers the risk of adopting AI; the risk of others' AI belongs on the enterprise threat and cyber register, with a different owner and a different control set. Source of the challenge: COSO GenAI 2026 names deepfakes and synthetic records as a fraud vector under Principle 8. Decision August 2026.

**AGI / existential / loss-of-control at frontier**  
Out of scope for an enterprise operational map; operational shadow captured in Domain 12. Add only for a frontier-developer audience.

**Generic IT / cyber / vendor risk**  
Excluded by the incremental-risk lens — already on every enterprise register.

**Macro labor-market / societal-scale economics**  
Kept only the slice the enterprise owns (its workforce, its reputation).

**Pure controls and threats**  
Excluded by form; entries are risk factors — conditions and failure modes — never a control ('MFA') or a threat actor ('an attacker').


### Retained when challenged

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


### Considered and not added

**Shared accountability across the AI stack — as a separate factor**  
SOURCE: CoSAI AI Shared Responsibility Framework; CSA AICM five-layer ownership model; an external reviewer; and the framing that cloud needed a shared RESPONSIBILITY model (who does what) while AI needs a shared ACCOUNTABILITY model (who answers when an agent acts). PROPOSED as a new D1 factor. WITHDRAWN on challenge: the proposed poster label read as a restatement of AIRM-006, whose wording never said 'internal'. RESOLVED by expanding AIRM-006 to name the cross-party stack and the shift of accountability with autonomy.

**Authorizer versus actor — preserving who authorized an agent's action and which agent performed it**  
SOURCE: external reviewer, quoting a control requirement. PROPOSED as a new D12 factor. WITHDRAWN on challenge: AIRM-109 owns the mechanism (inadequate logging) and AIRM-187 the outcome (accountability gap); the proposal differed from 109 only in which field the log omits. Control granularity presented as a risk. RESOLVED by adding 'and the human authorization behind them' to AIRM-109.

**Classification of agent autonomy levels**  
SOURCE: CoSAI AI SRF, via external reviewer. DECLINED: a classification scheme is a control (form rule 3.1). The underlying risk is carried by AIRM-175 and the expanded AIRM-006.

**Agent authority as the intersection of mandate, purpose, task, resource policy, and risk context**  
SOURCE: external reviewer. DECLINED: a least-privilege principle, i.e. a control. Risk faces carried by AIRM-177 and AIRM-175.

**Penetration-testing firms routing client vulnerability data through frontier models**  
SOURCE: external reviewer's own risk-acceptance decision. DECLINED as a factor: an instance of AIRM-142, AIRM-041 and AIRM-150. Retained here as a workshop example.

**D12 — Autonomy & Delegated Action named as a risk type, not a residual/other domain**  
CHALLENGE (external review, July 2026): Domain 12 was an axis inconsistency — Domains 1-11 are enterprise functions, D12 was a technology pattern. RESOLVED pre-release by renaming it to the risk type rather than justifying the exception, and by recording the DOMAIN ROUTING RULE (Design Guide 2.3): a technology pattern does not earn a domain; a new domain is justified only when a RISK TYPE has no home on the axis. CLOSED August 2026 — the challenging reviewer accepted the resolution, noting that justifying D12 as residual 'still leaves you explaining an exception' whereas naming it to the risk type removes it, and confirming the rule handles multimodal and RAG when they arrive. Recorded because this is the map's most-challenged structural decision.

**D1/D12 accountability pair — corroborated independently**  
The two-faced split between D1 'Failure to define accountability for autonomous / agent-driven decisions' and D12 'Accountability gap for harm caused by autonomous action' was reported as a duplicate by an external reviewer, who withdrew the report on learning it was documented (the reviewer had worked from the poster, where only the marker is visible — a discoverability failure, since addressed by adding a sheet guide to every tab). The same reviewer then reported reaching the same split independently while building a separate governance product, one face landing as a system-level risk and the other as an organizational capability gap. Convergence from a different construction method is stronger evidence than the original design argument.

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
SOURCE: CSA CISO post-mortem recommendation to use identifiable source IP ranges with PTR records. DECLINED: this is a CONTROL, not a risk. Excluded by form rule 3.1 — factors are outcomes or conditions, never controls.

**No response capability for the case where your own agent harms a third party**  
SOURCE: CSA CISO post-mortem recommendation to stand up two separate agentic response teams (victim and perpetrator). DECLINED: a control. The underlying risks are covered by D10 'Harm to non-users and third parties', D8 'Liability for harm caused by AI decisions or outputs', and D7 incident management.

**Inability to mass-rotate credentials or rebuild clusters at scale**  
SOURCE: CSA CISO post-mortem recommendations on ephemeral credentials and immutable infrastructure. DECLINED: generic resilience engineering. Fails the Gate B bounding principle — the delta is 'faster', which is not a specific nameable AI mechanism.

**Control degradation as the AI system and its integrations change — ADDED pre-release**  
SOURCE: raised in review of the containment factor. Guardrails, access scopes, evaluation thresholds, and approval gates drift as models are updated, tools added, and integrations grow, so controls are re-verified less often than the system changes. ASSESSMENT: clears the Gate B bounding principle. Held back from an earlier pre-release iteration on size grounds (Domain 7 already heavy). RESOLVED pre-release: measuring the reference-map benchmark from source showed a per-category range of 1-5 with max 5, so a fifth factor in Change & lifecycle sits within the reference range. Added.


---

## Change log (factor grain)

| Version | Date | Change | Factor ID(s) | Detail |
|---|---|---|---|---|
| v1.0 | September 2026 | baseline | — | Baseline established. All 189 factors and their identifiers are as of this release. Pre-release iteration is not carried here; identifiers assigned during pre-release were preserved. |

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
| G | X-ref | '→n' = this factor has another face owned by domain n. Human wayfinding hint; the Cross-references sheet is authoritative, by ID. |
| H | Status | 'active' or 'retired'. |
| I | Superseded by | When a factor is merged or replaced: the surviving ID. |

---

## Version history

Factor wording changes between versions. IDs do not. Cite IDs.

| Version | Date | Factors | What changed |
|---|---|---|---|
| **v1.0** | September 2026 | 189 | First public release. 12 domains, 54 categories, 189 risk factors, each with a permanent identifier (AIRM-001 onward). Structure: organized by the enterprise function that owns the risk, not by AI lifecycle. Scope: risk arising from the organization's own adoption of AI. Validation before release: crosswalked against 22 frameworks, regulations, and taxonomies; persona and named-expert critique; several rounds of external practitioner review; used as the validation standard for an independent 264-control catalog; and a full citation audit in which every named source locator was verified against the primary text and every factor tagged Original was checked against every cited framework. Result: 189 of 189 factors traceable; 98 carry the author's framing; 30 are named by no reviewed framework. From this version, changes are recorded at factor grain on the Change log sheet, and identifiers never change. |

---

## Sources

NIST AI RMF & GenAI Profile · EU AI Act · ISO/IEC 42001 · OWASP LLM & Agentic Top 10 · OWASP AISVS 1.0 · MITRE ATLAS · Databricks DASF v3.0 · Databricks AI Governance Framework · COSO Internal Control over GenAI (2026) · CRI FS-AI-RMF v1.0 · CSA AICM v1.1 · MIT AI Risk Repository · Intl AI Safety Report · Weidinger/Shelby taxonomies · Colorado AI laws · SR 11-7

Databricks DASF and AI Governance Framework are © Databricks, licensed CC BY-SA 4.0.


---

*AI Risk Map v1.0 · © 2026 Evan Wheeler · CC BY-SA 4.0. If you build on this, attribution and share-alike apply.*
