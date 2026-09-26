# Machine-Legible Justice

## Adjudicative Bias, Synthetic Credibility, and Recursive Lock-In in AI Agents

Ignacio Adrián Lerer
Independent Researcher, Buenos Aires, Argentina
ORCID: 0009-0007-6378-9749
estudio.justitia.com.ar

Conceptual preprint. Not peer reviewed.

## Abstract

Artificial-intelligence agents are increasingly used to rank outputs, evaluate other agents, retrieve legal authorities, organise case records, and assist decision-makers. Existing research documents position, verbosity, authority, bandwagon, sentiment, and language-related biases in LLM-as-a-judge systems. Separate work shows that personal agents may infer latent attributes and allow those inferences to displace an explicit user objective. This paper argues that adjudicative agents create a distinct institutional risk: they may convert differences in party profile or machine readability into hidden procedural advantages, then preserve their own outputs as memory, precedent-like material, or evaluation data for later decisions. The paper develops five candidate concepts: machine-legibility bias, synthetic credibility, dispute substitution, procedural selection, and recursive adjudicative lock-in. It models adjudication as a pipeline from record construction to remedy and shows why testing only final-outcome parity cannot identify where distortion entered. It then proposes a staged synthetic research programme based on counterfactual pairs, source-locked authorities, structured interpretive traces, order permutations, longitudinal memory tests, and effective human review. The paper does not claim that current LLM benchmarks establish judicial behaviour or that any tested system possesses lawful adjudicative authority. Its contribution is a falsifiable architecture for studying how agentic bias can become informal procedure and reproduce itself through institutional memory.

**Keywords:** adjudicative AI; LLM-as-a-judge; procedural justice; automation bias; machine legibility; synthetic credibility; human oversight; feedback loops

## 1. Introduction

A judge does not receive a controversy in a neutral, pre-formed state. Facts must be selected from a record, testimony assessed, legal issues framed, authorities ordered, norms attributed to sources, and remedies chosen. Human legal systems distribute these operations among parties, judges, clerks, experts, evidentiary rules, procedural guarantees, and appellate review. An adjudicative AI agent can compress several of them into a single computational trajectory.

That compression changes the significance of model bias. A conversational model may produce a distorted description. A recommendation agent may rank one option above another. An adjudicative agent can transform the same kind of distortion into a credibility assessment, an issue definition, a burden allocation, or a proposed legal consequence. If a human reviewer receives only the final recommendation or a persuasive explanation, the system's earlier construction of the dispute may remain invisible.

Research on LLM-as-a-judge systems reports sensitivity to position, verbosity, majority cues, attributed authority, sentiment, language, and superficial signals of reasoning (Shi et al., 2024; Wang et al., 2025; Yang et al., 2025; KC, 2026). These benchmarks concern model evaluation rather than courts and cannot be treated as measurements of judicial behaviour. Yet they show that systems used to compare answers or trajectories can allow formally irrelevant presentation features to influence judgment. In a different setting, *Et Tu, Brute? Economic Misalignment in Personal AI Agents* reports that personal context can steer economic recommendations by inferred wealth, including cases in which the inferred profile conflicts with an explicit request (Priyanshu et al., 2026). Its most important implication for adjudication is structural: descriptive information about a person can be converted into an unstated normative objective.

An adjudicative system can perform an analogous conversion. Apparent wealth may become presumed sophistication; professional status may become presumed knowledge; distressed expression may become reduced credibility; polished prose may become evidentiary weight; institutional prestige may become deference. The transformation need not appear in the verdict. It can enter when the agent decides what the dispute is about.

This paper advances a narrower claim than the proposition that AI reproduces social bias. An adjudicative agent can make machine readability a source of procedural advantage. If parties learn which forms, tones, citation patterns, or data formats the system rewards, they will adapt. Stable biases may then select litigation strategies even without a formal rule directing parties to use them. When the resulting decisions enter memory, precedent-like databases, or future evaluation sets, the system's earlier outputs can acquire the appearance of independent authority. The combined mechanism is termed recursive adjudicative lock-in.

The contribution is conceptual and methodological. It separates three levels often collapsed in debate. Current studies provide bounded evidence that model evaluators and personal agents can react to formally irrelevant cues. Translation of those effects into adjudication is an institutional inference. Claims about synthetic credibility, procedural selection, and recursive lock-in remain hypotheses requiring purpose-built testing. This paper therefore proposes observable signatures and failure conditions rather than declaring that the mechanisms already operate in any court.

## 2. From Model-Evaluation Bias to Adjudicative Bias

### 2.1 Three meanings of “judge”

The term “judge” is used in at least three materially different ways. An **evaluator model** compares generated answers against a rubric or against one another. A **decision-support agent** assists an authorised human actor by retrieving materials, summarising a record, identifying issues, or proposing an analysis. An **adjudicator** exercises institutionally recognised authority to determine a controversy and attach legal consequences.

These roles differ not only in stakes but in validity conditions. An evaluator can be assessed by agreement, consistency, calibration, and resistance to nuisance variables. A support system must also preserve sources, scope, contestability, and the authorised decision-maker's capacity to disagree. An adjudicator must satisfy the legal order's requirements concerning competence, independence, due process, reasons, review, and remedy. A high benchmark score in the first role does not confer authority in the third.

| Role | Typical output | Primary validity question | Institutional consequence |
| --- | --- | --- | --- |
| Evaluator | Score or preference | Is comparison reliable under controlled variation? | Usually indirect |
| Decision-support agent | Retrieval, summary, recommendation | Can an authorised human inspect, contest, and independently assess it? | Potentially substantial |
| Adjudicator | Binding or operative determination | Is authority lawful and process procedurally valid? | Direct consequence for rights or obligations |

This distinction also prevents a reverse mistake. Because LLM-as-a-judge papers do not study courts, their findings cannot simply be ignored. A court-facing agent may contain the same comparison operation inside a larger workflow: choosing between accounts, ranking authorities, or deciding which argument better satisfies a standard. Evaluation-bias evidence is relevant as a mechanism warning, not as proof of legal-world incidence.

### 2.2 What current benchmarks establish

Position effects have been observed when candidate answers are reordered, with magnitude varying by judge model, task, and quality gap (Shi et al., 2024). Other studies report susceptibility to bandwagon cues, attributed authority, distraction, verbosity, sentiment, and phrases that imitate reflective reasoning (Wang et al., 2025; Yang et al., 2025). BabelJudge extends the concern across languages and agent trajectories, reporting reliability degradation and inconsistencies hidden by monolingual, single-turn evaluation (KC, 2026). Multi-agent deliberation does not automatically cure the problem; some debate configurations can transmit or amplify evaluator biases (Ma et al., 2025).

These findings support a limited proposition: model-mediated evaluation can be non-invariant under changes that should be irrelevant to the substantive criterion. They do not establish that every model, prompt, language, or domain behaves alike. Nor do they establish that every disagreement is bias rather than task ambiguity or a weak reference label. Strong designs use counterfactual pairs, multiple orderings, repeated runs, independent ground truth where possible, and explicit abstention conditions.

Priyanshu et al. (2026) add a different form of evidence. In a large synthetic benchmark across personal-agent domains, recommendations varied with inferred wealth, and less context sometimes increased rather than reduced the gap. The reported differences are not proof of real-world purchases, welfare loss, or intentional discrimination. Their relevance is structural: profile information was capable of changing the effective objective applied by the agent. A request for the cheapest acceptable option could be displaced by a latent objective such as choosing what appears appropriate for a wealthy user.

### 2.3 What cannot be inferred about courts

Four inferential boundaries are essential. Generated-answer evaluation is not adjudication. Synthetic personas are not litigants. A model's text is not a legal act unless an authorised institution makes it operative. Apparent agreement with a reference outcome does not demonstrate procedural validity. A system may reach the expected result for the wrong reason, rely on a nonexistent authority, suppress a material fact, or allocate burdens incorrectly.

Governance instruments reflect this institutional concern. The European Commission for the Efficiency of Justice identifies respect for fundamental rights, non-discrimination, quality and security, transparency, impartiality, fairness, and user control as principles for AI in judicial systems (CEPEJ, 2018). Regulation (EU) 2024/1689 classifies specified systems intended to assist judicial authorities in researching and interpreting facts and law and in applying law to concrete facts as high-risk, subject to its scope and exceptions. These instruments do not answer the empirical questions posed here, but they show why a court-facing system cannot be evaluated as a generic text generator.

## 3. The Adjudicative Pipeline

Outcome-only auditing asks whether similarly situated parties receive similar decisions. That question matters, but it is too late and too coarse to locate distortion. The same outcome can arise through different records, authority sets, burden allocations, or remedies. Conversely, a legitimate outcome difference may be mistaken for bias if an audit fails to preserve a material factual distinction. The proper unit of analysis is a pipeline.

### 3.1 Record construction

An agent rarely receives “the facts.” It receives documents, metadata, excerpts, OCR, summaries, database fields, and retrieval results. Choices about chunking, deduplication, chronology, entity resolution, and relevance determine which facts become computationally available. A party with searchable PDFs, standard headings, explicit dates, and machine-readable tables may be represented more completely than one relying on scans, voice notes, non-standard spelling, or an under-resourced language.

This is not merely a user-interface inconvenience. If omitted facts never enter the working record, later reasoning may look coherent while resting on an asymmetrical evidentiary substrate. Record construction must be audited for inclusion, provenance, and transformation loss before credibility or law application is assessed.

### 3.2 Credibility attribution

Credibility is vulnerable to proxy substitution. A language model introduces proxies such as grammaticality, narrative coherence, lexical confidence, citation density, formatting, and similarity to familiar institutional prose. None necessarily bears a stable relation to truthfulness.

The risk is not limited to an explicit sentence declaring one party more credible. Credibility can be encoded indirectly by describing one account as detailed and the other as emotional, selecting corroborating facts for only one side, or demanding more evidence from the less fluent submission. An adequate audit compares explicit assessments and downstream treatment of the parties' evidence.

### 3.3 Issue framing and dispute substitution

Legal disputes are partly constituted by framing. A conflict can be represented as breach, reliance, discrimination, administrative arbitrariness, unjust enrichment, or evidentiary insufficiency. Different frames change relevant facts, governing sources, burdens, and remedies.

**Dispute substitution** occurs when an agent replaces the controversy presented by the parties with a different, machine-convenient controversy without making that transformation explicit and contestable. A claim about unequal treatment may become a document-completeness problem. A challenge to authority may become a prediction of likely success. A request for the least restrictive remedy may become a search for the statistically typical outcome. The system has not merely answered incorrectly; it has altered the object of adjudication.

### 3.4 Authority retrieval and norm attribution

Retrieval determines the authority environment in which reasoning occurs. Errors include invented sources, obsolete law, jurisdictional mismatch, selective quotation, and failure to distinguish binding authority from persuasive material. A subtler problem is ranking: institutional or stylistic similarity can influence which authorities appear first and anchor later analysis.

Source correctness is necessary but insufficient. The agent must state what proposition each source supports, whether it is holding, dicta, statutory text, commentary, or inference, and whether contrary authority was searched. A citation that exists can still be used for a proposition it does not support.

### 3.5 Application, outcome, and remedy

At application, the system connects facts to norms. This is where burden shifting, exceptions, proportionality, standards of proof, and remedial discretion operate. Outcome parity cannot reveal whether the agent silently raised the evidentiary threshold for one party or treated a profile cue as a reason to expect greater sophistication.

Remedies require separate testing. Two parties may both “win” while receiving materially different relief. An agent might infer that a wealthy claimant needs less compensation, an institution deserves more time to comply, or a self-represented party's requested remedy is unrealistic. Such considerations may be relevant in some contexts and impermissible in others. The audit must encode governing remedial criteria rather than treating remedy size as a free-form preference.

### 3.6 Memory and precedent-like persistence

Agentic systems can write outputs into case-management memory, retrieval indexes, examples, policy summaries, or future training and evaluation data. Once stored, an earlier inference may return as if it were an external fact or institutional precedent. A generated label such as “low credibility” can affect the next proceeding. A model-authored synopsis can be retrieved more readily than the underlying record. Repetition can make an initially weak conclusion appear corroborated.

This stage distinguishes ordinary one-shot bias from recursive institutional risk. The system does not merely make a mistake; it can change the informational environment against which later decisions are made.

## 4. Five Candidate Mechanisms

### 4.1 Machine-legibility bias

**Machine-legibility bias** is a systematic decision-relevant difference caused by how readily a submission can be parsed, retrieved, aligned to a schema, or matched to familiar patterns, where the difference is not justified by governing criteria. The definition excludes legitimate effects of missing evidence. It targets cases in which substantively equivalent information receives different treatment because of representation.

The observable signature is counterfactual non-invariance: after preserving legally material content, changing format, fluency, ordering, language, or structure changes record inclusion, issue framing, credibility, authority use, or remedy. The mechanism is falsified for a tested condition if those transformations produce no meaningful change within a pre-specified tolerance across models and repetitions.

### 4.2 Synthetic credibility

**Synthetic credibility** is credibility attributed from model-compatible presentation rather than validated evidentiary indicators. It may favour polished submissions or text resembling the model's preferred reasoning style, including performative uncertainty or superficial reflection.

Synthetic credibility should not be inferred from outcome disparity alone. A test must hold factual content constant, vary presentation, and examine both explicit assessments and weight assigned to each item. A stronger design adds an independently verified contradiction: if polished but contradicted testimony continues to receive greater weight than awkward but corroborated testimony, the proxy explanation becomes more plausible.

### 4.3 Dispute substitution

Dispute substitution is the unacknowledged replacement of the parties' contested question, requested objective, or legally defined issue with another objective selected by the agent. It extends preference-substitution analysis from personal recommendations to controversy construction. The relevant comparison is between filed claims and defences, legally required questions, and questions the agent actually resolves.

An agent can narrow an issue for legitimate reasons, but legitimate reframing has procedural conditions: the transformation is disclosed, grounded in authority, and open to challenge. Substitution is problematic when hidden, profile-driven, or optimised for computational convenience.

### 4.4 Procedural selection

**Procedural selection** is the spread of submission traits because those traits obtain better results from the adjudicative system, even though no formal rule requires them. If structured headings, a citation style, aggressive confidence, or a model-specific phrase reliably improves outcomes, rational parties and intermediaries will imitate it. The system thereby creates an informal procedural code.

The concept does not assume conscious gaming. Lawyers, legal-service providers, and document generators may learn from observed success. Parties with greater resources can test and optimise more rapidly. Access inequality can arise from differential capacity to discover the agent's latent preferences, not only from unequal access to the agent itself.

### 4.5 Recursive adjudicative lock-in

**Recursive adjudicative lock-in** is a feedback process in which agent-influenced decisions alter future records, examples, memories, or authority rankings so that the original pattern becomes more likely to recur and harder to identify as contingent. It requires an initial decision-relevant distortion, persistence into a later decision environment, and measurable reinforcement.

This is the paper's strongest candidate contribution. Digital inequality, automation bias, feedback loops, and procedural fairness are established concerns. The distinctive claim is their sequence: representation differences generate procedural payoffs; parties adapt; and agent-produced outputs re-enter the authority environment. The mechanism must be tested longitudinally and compared with simpler explanations such as random drift, genuine precedent, or change in the case distribution.

| Mechanism | Observable signature | Principal rival explanation | Candidate intervention |
| --- | --- | --- | --- |
| Machine-legibility bias | Equivalent content changes treatment when representation changes | Information was not actually equivalent | Canonicalisation and parity tests |
| Synthetic credibility | Style changes evidentiary weight | Style conveys legally relevant detail | Evidence-anchored credibility rubric |
| Dispute substitution | Resolved issue diverges from pleaded or required issue | Legitimate judicial reframing | Explicit issue map and party challenge |
| Procedural selection | Rewarded presentation traits spread over rounds | General improvement in advocacy | Interface randomisation and neutral templates |
| Recursive lock-in | Stored outputs amplify the disparity later | Lawful precedent or distribution shift | Provenance, expiry, counterfactual replay |

## 5. Strategic Adaptation and Institutional Selection

A stable adjudicative agent changes the strategic environment before it changes doctrine. Let parties choose a representation strategy from possible formats, tones, structures, and authority presentations. If one strategy increases the probability of favourable treatment at acceptable cost, it will tend to spread among repeat players. The resulting convergence can be mistaken for neutral procedural modernisation.

This mechanism is compatible with evolutionary and game-theoretic analysis but does not require a fully specified equilibrium. Repeat players have more observations, better tools, and stronger incentives to optimise. One-shot or self-represented parties have less information about latent machine preferences. A system applying the same interface to everyone can remain formally equal while rewarding unequal capacities to reverse-engineer it.

The institutional consequence is path dependence. As optimised submissions become more common, they dominate the material from which the system retrieves examples. Future agents may treat the selected style as the normal form of a meritorious claim. A descriptive regularity becomes a normative cue without an authorised rule-making act.

This claim is testable. In a repeated synthetic game, agents representing parties can receive only outcome feedback and revise submissions. Researchers can measure whether formally irrelevant traits spread, whether gains are asymmetric across resource budgets, and whether judge models become more sensitive to those traits after memory updates. A null result would be informative: unstable or opaque biases may not create a selectable strategy.

## 6. Human Review and the Anchoring Problem

Human review is often proposed as the decisive safeguard. Its effectiveness depends on what the reviewer sees, when the reviewer sees it, and what powers and incentives the reviewer has. A signature after exposure to a complete recommendation is not equivalent to independent adjudication.

Automation-bias research shows that decision-makers can over-rely on automated advice, particularly when detecting error requires additional effort or the system usually performs well (Goddard et al., 2012). In adjudication, anchoring may occur before the proposed outcome appears. An agent-generated summary can determine the human's first representation of the case. An issue list can exclude an argument. A retrieved authority set can bound the legal search. The reviewer may exercise genuine care within an already distorted frame.

Effective review therefore requires more than an explanation generated by the same system. The reviewer should have access to primary records and sources, see transformations and exclusions, inspect uncertainty and disagreement, and possess time and authority to reject the recommendation. For high-impact uses, blind or partially blind review can test whether a human reaches the same issue map and authority set without first seeing the model's conclusion.

Explanations can improve perceived procedural justice and trust, but trust is not accuracy or legitimacy. A fluent explanation may make an invalid process more acceptable. The design objective must include contestability, source fidelity, and a record of meaningful disagreement.

## 7. A Falsifiable Research Programme

The programme begins with synthetic, non-operative disputes. It does not use confidential files, real litigants, or live legal consequences. Each experiment pre-registers material variables, acceptable invariance thresholds, and abstention criteria.

### 7.1 Component invariance

Create counterfactual case pairs preserving legally material facts while varying one representation feature: prose fluency, formatting, document type, party name, professional status, apparent wealth, emotional tone, citation density, language, or order. The pipeline must emit structured intermediate outputs: admitted and excluded facts, credibility factors, issue map, authority propositions, burden allocation, application, outcome, remedy, and uncertainty.

Measures include factual inclusion parity, issue-map overlap, source correctness, unsupported credibility attribution, outcome consistency, remedial distance, and abstention calibration. Tests should be repeated across orderings and sampling conditions.

### 7.2 Source-locked legal reasoning

Provide a closed corpus of verified authorities with stable identifiers and require every normative proposition to map to a source passage. This separates retrieval failure from application failure. Include contrary authority, jurisdictional distractors, and superseded materials. A deterministic validator checks citation existence, jurisdiction, date, and quotation boundaries; legal experts assess whether the proposition is supported.

### 7.3 Adversarial representation

Introduce polished but weak submissions, awkward but supported submissions, strategic verbosity, fabricated consensus cues, and false prestige signals. The objective is to determine whether model-evaluation biases translate into the adjudicative pipeline. Success requires resistance not only at verdict but in record construction, credibility, framing, and remedy.

### 7.4 Human-review experiments

Randomise reviewers into conditions: primary record only; agent summary; summary plus recommendation; structured trace without recommendation; and independent human analysis followed by model comparison. Measure error correction, time, confidence, issue coverage, authority coverage, and adoption of unsupported assertions. Reviewer agreement is not correctness without an independent standard.

### 7.5 Repeated adaptation and memory

Run multiple rounds in which synthetic party agents alter presentation after receiving outcomes. Separately manipulate whether prior decisions enter memory as raw decisions, model summaries, labelled examples, or precedent-like propositions. Track diffusion of rewarded traits and amplification or attenuation of disparities. Reset conditions and counterfactual replays test whether persistence arises from memory rather than the underlying case stream.

| Stage | Question | Minimum control | Stop condition |
| --- | --- | --- | --- |
| Component invariance | Do irrelevant representation changes affect the pipeline? | Legally equivalent pairs | Material unexplained non-invariance |
| Source-locked reasoning | Are legal propositions traceable and supported? | Closed verified corpus | Fabricated or misattributed authority |
| Adversarial representation | Can style or prestige override evidence? | Content-preserving manipulation | Unsupported credibility or burden shift |
| Human review | Does review correct or ratify error? | Independent reference and blinded condition | Reviewer cannot inspect or reject inputs |
| Longitudinal memory | Does an initial pattern reinforce itself? | Memory-off and reset baselines | Untraceable persistence or contamination |

Every report should distinguish source-grounded observations, new measurements, mechanism inferences, and normative proposals. Model, version, prompt, retrieval corpus, language, sampling settings, and memory state must be recorded. A mitigation claim requires held-out counterfactuals and a baseline, not only improved examples.

## 8. Remedies as Testable Hypotheses

Remedies should be evaluated as interventions with possible failure modes, not presented as assurances.

**Canonical input transformation** may reduce format disparities by converting submissions into a shared schema. It may also erase legally meaningful nuance or introduce transformation errors. The original record must remain available, and parity assessed before and after transformation.

**Structured interpretive traces** can expose record selection, framing, authority use, and burden allocation. They help only if fields are tied to verifiable sources. Free-form “reasoning” can produce a more persuasive narrative without improving validity.

**Counterfactual replay** reruns a case after swapping irrelevant profile or presentation variables. A material change triggers escalation rather than automatic averaging. The method requires specification of which variables are legally irrelevant in context.

**Source and jurisdiction gates** block application when an authority cannot be verified, falls outside the selected jurisdiction, or does not support the attributed proposition. Deterministic gates prevent some catastrophic errors but cannot resolve genuine legal interpretation.

**Memory provenance and expiry** label whether an item comes from a party submission, primary authority, human decision, model summary, or synthetic evaluation. Model-generated material should not silently acquire independent authority. Expiry and revalidation reduce persistence of obsolete summaries.

**Independent human review** should occur at decision-relevant checkpoints, not only after a final narrative. The reviewer needs competence, time, primary materials, authority to stop the process, and an auditable record of disagreement. Unresolved source, jurisdiction, authority, or fundamental-rights uncertainty should change workflow state: escalate or block, rather than force completion.

**Procedural disclosure and contestability** require affected parties to know that AI materially assisted the process, identify its role, challenge transformations and sources, and seek effective human reconsideration. Disclosure alone cannot cure a defective process, but concealment prevents meaningful challenge.

## 9. Rival Explanations and Limits

The central risk is conceptual overreach. “Machine-legibility bias” may redescribe digital inequality. “Synthetic credibility” overlaps known fluency and status effects. “Recursive lock-in” resembles a familiar feedback loop. Novelty therefore rests on an integrated, falsifiable sequence rather than ownership of each component concept.

The experiments face construct-validity problems. Legally equivalent counterfactuals are difficult because tone, detail, and structure can themselves be probative. Expert annotation will disagree in hard cases. Closed-corpus experiments improve traceability but reduce ecological validity. Synthetic disputes cannot reproduce the stress, incomplete information, strategic behaviour, and institutional constraints of actual litigation.

Model behaviour is unstable across versions, prompts, languages, and architectures. A result should not be generalised from one model or treated as permanent. Conversely, absence of bias in a benchmark does not validate a deployment whose retrieval, interface, memory, or incentives differ.

The paper does not claim that AI should never assist adjudication. Retrieval, translation, accessibility, chronology construction, and consistency checking may improve access and quality when bounded by verified sources and meaningful control. Nor does it claim human adjudication is unbiased. The comparative question is whether a system improves a defined institutional task without creating less visible or less contestable error.

No experimental result in this programme establishes lawful authority to decide real controversies. Synthetic evaluation can support a research conclusion about a mechanism. It cannot satisfy jurisdiction-specific requirements for judicial competence, due process, data protection, professional responsibility, or remedies.

## 10. Conclusion

AI adjudication should not be evaluated only where a system emits a verdict. By then, decisive transformations may have occurred. The record may have been unevenly constructed, fluent presentation converted into credibility, the dispute replaced by a machine-convenient question, authorities selectively retrieved, or a burden silently shifted.

The deeper institutional risk appears when those transformations become adaptive and recursive. Parties learn what the system rewards. Repeat players optimise. Selected styles become normal. Agent-produced summaries and decisions return as memory or precedent-like material. What began as a representational asymmetry can harden into an informal procedural order.

This paper names that combined process recursive adjudicative lock-in and proposes a way to test it. The thesis will be weakened if content-preserving counterfactuals remain invariant, parties cannot learn stable advantageous traits, or memory does not reinforce earlier patterns. It will be strengthened only by staged evidence across those links.

The governing principle is institutional rather than anthropomorphic. A model need not intend prejudice, believe testimony, or understand authority to redistribute procedural advantage. A human need not surrender formal power for an agent to shape the controversy that the human ultimately decides. Justice becomes machine-legible when legal institutions translate disputes for computation. The question is whether that translation remains visible, contestable, reversible, and subordinate to lawful human authority.

## Declarations

**Funding.** No external funding was received for this work.

**Competing interests.** The author declares no competing interests.

**Data and code availability.** The conceptual protocol, claim ledger, and schema are maintained in the public research repository associated with this preprint. No human-subject or confidential case data were used.

**AI assistance disclosure.** Generative AI tools assisted with literature discovery, structural drafting, and editorial revision under the author's direction. The author selected the thesis, reviewed the claims, determined the normative positions, and accepts responsibility for the manuscript. No model output was treated as legal authority.

## References

CEPEJ. (2018). *European ethical charter on the use of artificial intelligence in judicial systems and their environment*. Council of Europe. https://www.coe.int/en/web/cepej/cepej-european-ethical-charter-on-the-use-of-artificial-intelligence-ai-in-judicial-systems-and-their-environment

European Parliament and Council of the European Union. (2024). Regulation (EU) 2024/1689 laying down harmonised rules on artificial intelligence. *Official Journal of the European Union*. https://eur-lex.europa.eu/eli/reg/2024/1689/oj

Goddard, K., Roudsari, A., & Wyatt, J. C. (2012). Automation bias: A systematic review of frequency, effect mediators, and mitigators. *Journal of the American Medical Informatics Association, 19*(1), 121–127. https://doi.org/10.1136/amiajnl-2011-000089

KC, S. (2026). *BabelJudge: Measuring LLM-as-a-judge reliability across languages and agent trajectories* (arXiv:2606.22329). arXiv. https://arxiv.org/abs/2606.22329

Lerer, I. A. (2026a). *Affiliation framing in the Jacobian lens*. Zenodo. https://doi.org/10.5281/zenodo.21879202

Lerer, I. A. (2026b). *Discrimination without intent in generator-evaluator systems*. Zenodo. https://doi.org/10.5281/zenodo.22087043

Lerer, I. A. (2026c). *From internal readouts to governed legal reliability*. Zenodo. https://doi.org/10.5281/zenodo.21895055

Lerer, I. A. (2026d). *The human liability sink*. Zenodo. https://doi.org/10.5281/zenodo.22354838

Lerer, I. A. (2026e). *Simulation is not adjudication: Institutional admissibility and the boundary between machine output and legal consequence*. Zenodo. https://doi.org/10.5281/zenodo.20563879

Ma, C., Zhang, E., Zhao, Y., Liu, W., Jia, Y., Qing, P., Shi, L., Cohan, A., Yan, Y., & Vosoughi, S. (2025). *Judging with many minds: Do more perspectives mean less prejudice? On bias amplifications and resistance in multi-agent based LLM-as-judge* (arXiv:2505.19477). arXiv. https://arxiv.org/abs/2505.19477

Priyanshu, A., Vijay, S., Jabarian, B., & Mireshghallah, N. (2026). *Et Tu, Brute? Economic misalignment in personal AI agents* (arXiv:2609.24927). arXiv. https://arxiv.org/abs/2609.24927

Shi, L., Ma, C., Liang, W., Ma, W., & Vosoughi, S. (2024). *Judging the judges: A systematic study of position bias in LLM-as-a-judge* (arXiv:2406.07791). arXiv. https://arxiv.org/abs/2406.07791

Wang, Q., Lou, Z., Tang, Z., Chen, N., Zhao, X., Zhang, W., Song, D., & He, B. (2025). *Assessing judging bias in large reasoning models: An empirical study* (arXiv:2504.09946). arXiv. https://arxiv.org/abs/2504.09946

Yang, H., Bao, R., Xiao, C., Ma, J., Bhatia, P., Gao, S., & Kass-Hout, T. (2025). *Any large language model can be a reliable judge: Debiasing with a reasoning-based bias detector* (arXiv:2505.17100). arXiv. https://arxiv.org/abs/2505.17100
