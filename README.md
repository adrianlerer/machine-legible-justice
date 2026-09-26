# Machine-Legible Justice

## Adjudicative Bias, Synthetic Credibility, and Recursive Lock-In in AI Agents

This repository develops a source-bounded conceptual and experimental research programme on AI agents used to evaluate, assist with, or adjudicate controversies.

The central question is not merely whether an AI judge can reproduce human bias. It is whether an agentic adjudication system can turn differences in wealth, status, language, presentation, or machine readability into hidden procedural advantages, then preserve its own decisions as evidence for future decisions.

## Core thesis

An adjudicative agent does not receive a dispute in a neutral, pre-formed state. It constructs the dispute through a pipeline:

```text
parties
  -> selected facts
  -> attributed credibility
  -> framed legal issue
  -> retrieved authorities
  -> attributed norm
  -> application
  -> remedy
  -> memory or precedent
```

Bias at any stage can become operational when the system has authority to rank claims, recommend outcomes, allocate remedies, or shape the record reviewed by a human decision-maker.

## Proposed contributions

The project introduces five candidate concepts that remain subject to literature and novelty review:

1. **Machine-legibility bias:** legally equivalent claims receive different treatment because one is easier for the system to parse, retrieve, or fit into a familiar category.
2. **Synthetic credibility:** fluency, structure, professional tone, or data format is treated as evidence of truthfulness or reliability.
3. **Dispute substitution:** the system silently replaces the controversy raised by the parties with a different question that is easier to classify or resolve.
4. **Procedural selection:** parties adapt their submissions to the traits rewarded by the adjudicative agent, creating an informal machine-facing procedure.
5. **Recursive adjudicative lock-in:** biased outputs enter memory, precedent, evaluation, or training data and later appear as independent support for the same pattern.

These are research hypotheses, not established empirical findings and not statements of current law.

## Repository map

- [`paper/manuscript.md`](paper/manuscript.md): full conceptual preprint for author review.
- [`release/Machine-Legible-Justice-Lerer-2026.docx`](release/Machine-Legible-Justice-Lerer-2026.docx): A4 DOCX, prepared for author review.
- [`release/Machine-Legible-Justice-Lerer-2026.pdf`](release/Machine-Legible-Justice-Lerer-2026.pdf): rendered PDF, 11 pages.
- [`research/novelty-audit.md`](research/novelty-audit.md): inherited, extended, and candidate-new claims.
- [`research/claims-evidence.md`](research/claims-evidence.md): claims and evidence states.
- [`protocol/experimental-program.md`](protocol/experimental-program.md): staged, synthetic evaluation plan.
- [`schemas/case-fixture.schema.json`](schemas/case-fixture.schema.json): proposed structure for controlled controversy fixtures.
- [`STATUS.md`](STATUS.md): publication and validation state.

## Boundaries

- No real litigant, client, court, or confidential case data.
- No claim that LLM-as-a-judge benchmarks establish judicial validity.
- No automated adjudication of real rights, sanctions, money, liberty, or legal status.
- No external model runs are authorised by this repository.
- No private prompts, thresholds, product details, or internal Atlas materials are included.

## Author

Ignacio Adrián Lerer  
Independent researcher  
[estudio.justitia.com.ar](https://estudio.justitia.com.ar)

## Current state

`AUTHOR-REVIEW DRAFT / DOCX AND PDF READY / NOVELTY REVIEW OPEN / NO DOI YET`

Copyright remains with the author. No reuse licence has yet been selected. See [`LICENSE_PENDING.md`](LICENSE_PENDING.md).
