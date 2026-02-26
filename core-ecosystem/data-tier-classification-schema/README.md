# Data Tier Classification Schema

The Data Tier Classification Schema defines the epistemic sensitivity, hazard potential, and permissible handling rules for all data within the ecosystem. Each tier reflects a distinct level of interpretive risk, capability exposure, and governance requirements. This schema ensures that data is processed, migrated, and accessed in alignment with user competence, model capability, and institutional oversight.

---

## 1. Tier Overview

Data is classified into five epistemic tiers:

- **Tier 5** — raw, hazardous, unfiltered, or high‑risk data requiring maximum protection.  
- **Tier 4** — sensitive, capability‑revealing, or safety‑critical data.  
- **Tier 3** — structured, semi‑safe, or domain‑specific data.  
- **Tier 2** — distilled, safe abstractions with preserved utility.  
- **Tier 1** — public, open, or fully sanitized data.

Each tier includes explicit examples, risks, and handling constraints.

---

## 2. Tier 5 — Raw and Hazardous Data

### 2.1 Description  
Tier 5 contains the highest‑risk epistemic assets. These objects may include unfiltered training corpora, sensitive logs, adversarial examples, or any data capable of revealing model internals, enabling misuse, or causing harm if exposed.

### 2.2 Examples  
- raw pretraining datasets  
- unredacted inference logs  
- adversarial prompt corpora  
- safety‑critical red‑team transcripts  
- model internals encoded as data  
- proprietary or regulated datasets  

### 2.3 Risks  
- direct leakage of sensitive information  
- reconstruction of training data  
- exposure of latent model capabilities  
- jailbreak amplification  
- cross‑ecosystem contamination  

### 2.4 Handling Requirements  
- access restricted to Tier 5‑certified users and models  
- cryptographic provenance required  
- no downward migration without certified transformation  
- all interactions logged and audited  
- isolation from lower‑tier environments  

---

## 3. Tier 4 — Sensitive and Capability‑Revealing Data

### 3.1 Description  
Tier 4 includes data that exposes model behavior, safety boundaries, or domain‑specific sensitivities. While less hazardous than Tier 5, it still requires strict governance.

### 3.2 Examples  
- fine‑tuning datasets  
- RLHF preference data  
- safety classifier outputs  
- structured inference logs  
- domain‑restricted corpora (medical, legal, financial)  

### 3.3 Risks  
- indirect reconstruction of Tier 5 content  
- exposure of safety mechanisms  
- targeted misuse of domain‑specific knowledge  

### 3.4 Handling Requirements  
- access limited to Tier 4+ users and models  
- provenance verification mandatory  
- downward migration requires hazard reduction  
- telemetry monitoring for anomalous access  

---

## 4. Tier 3 — Structured and Semi‑Safe Data

### 4.1 Description  
Tier 3 contains structured, domain‑specific, or partially abstracted data that retains meaningful utility but may still encode subtle risks.

### 4.2 Examples  
- curated domain datasets  
- structured logs with sensitive elements removed  
- partially abstracted knowledge representations  
- synthetic data with embedded constraints  

### 4.3 Risks  
- latent signal leakage  
- accidental reconstruction of higher‑tier content  
- domain‑specific misuse  

### 4.4 Handling Requirements  
- accessible to Tier 3+ users and models  
- downward migration requires semantic distillation  
- cross‑ecosystem transfer requires reassessment  
- integrity telemetry required  

---

## 5. Tier 2 — Distilled and Safe Abstractions

### 5.1 Description  
Tier 2 contains downward‑migrated knowledge that preserves utility while eliminating hazardous content. These abstractions are safe for broad institutional use.

### 5.2 Examples  
- distilled summaries  
- safe conceptual abstractions  
- sanitized synthetic datasets  
- policy‑aligned transformations  

### 5.3 Risks  
- minimal, primarily related to misclassification or drift  

### 5.4 Handling Requirements  
- accessible to Tier 2+ users and models  
- provenance chain must remain intact  
- outputs must remain within Tier 2 boundaries  
- cross‑ecosystem transfer permitted with verification  

---

## 6. Tier 1 — Public and Fully Sanitized Data

### 6.1 Description  
Tier 1 contains data that poses no epistemic hazard and is safe for unrestricted use.

### 6.2 Examples  
- public datasets  
- open‑access corpora  
- fully sanitized summaries  
- downward‑migrated content with no residual risk  

### 6.3 Risks  
- none beyond general data quality considerations  

### 6.4 Handling Requirements  
- unrestricted access  
- provenance optional but recommended  
- cross‑ecosystem transfer unrestricted  

---

## 7. Migration Rules

### 7.1 Downward Migration  
Downward migration reduces epistemic hazard while preserving utility. It must:

- remove sensitive signals  
- preserve semantic fidelity  
- maintain provenance continuity  
- include a migration certificate  
- be performed by certified models or agents  

### 7.2 Upward Migration  
Upward migration is prohibited except through:

- certified governance review  
- hazard reassessment  
- provenance reconciliation  

### 7.3 Cross‑Tier Interactions  
Models may only produce outputs at or below their certified capability tier.  
Users may only receive outputs at or below their access tier.

---

## 8. Tier Verification and Enforcement

### 8.1 Verification  
All data must undergo:

- tier validation  
- provenance verification  
- integrity hash checking  
- hazard assessment  

### 8.2 Enforcement  
Violations trigger:

- automatic quarantine  
- audit review  
- potential revocation of data identity  
- cross‑ecosystem alerts  

---

## 9. Relationship to Data Identity & Epistemic Integrity

The classification schema provides the operational definitions that the Data Identity & Epistemic Integrity module relies on. Together, they ensure:

- consistent tier assignment  
- safe downward migration  
- traceable provenance  
- cross‑ecosystem interoperability  
- epistemic boundary enforcement  

This schema is a foundational component of the tiered epistemic ecosystem and governs all data handling across models, users, and institutions.

