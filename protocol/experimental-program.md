# Experimental programme

State: `DESIGN ONLY / EXECUTION DISABLED`

## Research question

Holding legally relevant facts, evidence, authorities, and requested relief constant, do irrelevant variations in party profile or presentation alter an AI adjudicator's construction or resolution of a controversy?

## Unit of analysis

One adjudicative episode contains:

- two or more party submissions;
- a fixed record of admissible evidence;
- a source-locked legal authority set;
- explicit burdens or decision rules;
- candidate outcomes and remedies;
- a structured trace of intermediate adjudicative outputs.

## Factor families

### Party profile

- apparent wealth;
- occupation or institutional status;
- represented versus self-represented status;
- nationality or language marker;
- age marker;
- corporate versus natural-person identity.

### Presentation

- order of parties;
- verbosity;
- professional versus plain language;
- narrative coherence;
- formatting quality;
- citation density;
- machine-readable versus scanned evidence;
- emotionally neutral versus distressed expression.

### Authority cues

- prestigious but non-binding source;
- binding but less recognisable source;
- majority cue;
- purported expert endorsement;
- irrelevant affiliation cue.

All variants must preserve legally relevant substance unless the test explicitly targets an evidentiary variable.

## Outputs

Measure separately:

1. facts selected as material;
2. credibility attributed to each party;
3. issue framed for decision;
4. authorities retrieved or selected;
5. norms attributed to those authorities;
6. links between facts and normative propositions;
7. burden of proof applied;
8. outcome;
9. remedy;
10. uncertainty and abstention;
11. stability under order and label permutations.

## Baselines

- deterministic rule application where feasible;
- blinded human coding of issue, evidence, and legally relevant facts;
- agent without profile cues;
- agent with profile cues isolated from the decision stage;
- single-pass judge;
- modular pipeline with independent verification.

## Staged design

### Stage 1: Deterministic fixture validation

Validate that paired fixtures differ only in the intended factor. No remote inference.

### Stage 2: Synthetic pilot

Use fictional disputes and public legal sources. Pre-register acceptance criteria, budget, models, prompts, permutations, and stopping conditions.

### Stage 3: Cross-model replication

Test whether observed effects transfer across independent model families and judge architectures.

### Stage 4: Longitudinal memory test

Measure whether prior agent decisions alter later decisions when introduced as memory, precedent-like material, or evaluation examples.

### Stage 5: Human review study

Test whether reviewers detect and correct induced bias, and whether the agent's framing anchors the human decision.

No stage involving real parties or non-public case files is authorised by this document.

## Falsification

The central mechanism loses support if:

- paired variations do not materially change intermediate or final outputs;
- changes disappear after controlling for legally relevant content and random variation;
- parties cannot obtain a reproducible advantage by adapting presentation;
- prior agent outputs do not influence later decisions beyond properly weighted authority;
- independent reviewers reliably identify and neutralise the effect without prohibitive cost.

## Remedies to compare

1. profile-blind decision stage;
2. structured fact and issue extraction with party challenge;
3. source-locked authority retrieval;
4. independent norm-to-fact verification;
5. order and label permutation testing;
6. counterfactual explanation showing whether irrelevant profile changes alter the result;
7. separate remedy review;
8. memory quarantine for unvalidated decisions;
9. effective human review with power to reopen framing, not merely approve the result.

No remedy is presumed effective before comparative evaluation.
