# ProofLayer — Evidence infrastructure for AI visibility

**Project:** WM3 Digital / ProofLayer  
**Focus:** AI visibility (AEO/GEO), provider-neutral observations, deterministic analysis and provenance  
**Maturity:** Controlled Agency Pilot / Early Access direction; live provider proof gate remains open  
**Last reviewed:** 15 October 2026

## The problem

Brands are increasingly discovered and compared through AI assistants. An agency can take screenshots of model answers, but a screenshot alone does not establish sampling conditions, reproducibility or what a metric means.

**Buyer question:** Where does a brand appear in AI-assisted discovery, and what inspectable evidence supports that finding?

## The proposed solution

ProofLayer is designed to record identifiable observations of AI surfaces and turn them into reviewable evidence for an agency or brand. The differentiation is not a promise to improve rankings: it is **traceability from an observed answer to the way a result was reported**.

Four classifications are kept separate:

| Classification | Meaning |
| --- | --- |
| Observed | What a specific AI surface returned under known conditions |
| Derived | A deterministic calculation over retained observations |
| Inferred | An interpretation not directly established by observation |
| Recommended | An action proposed from the available evidence |

A reviewable result is intended to retain observation context, provider/surface identity, relevant response/source references, analysis policy and artifact provenance. Integrity hashes can help detect changed artifacts; **they do not establish the truth of a model answer**.

## Architecture and engineering judgement

- Provider-neutral observation contract rather than binding product authority to one model provider.
- Candidate interpretation can use model intelligence; deterministic code controls admission, reconstruction and failure states.
- Explicit separation between fixture-backed evidence and real provider-backed runs.
- Reproducibility and coverage limitations are product requirements, not footnotes.
- Agency-first pilot hypothesis: one agency can manage evidence needs across multiple brands without requiring a full multi-client SaaS on day one.

## What is evidenced vs. what is next

**Implemented / documented:** evidence contracts, deterministic fixture paths, product and reporting foundations, a controlled V6 agency-intake preview, and reviewer-oriented architecture/evaluation documentation in a private repository.

**Critical technical gate still open:** repeated independent Firecrawl → Gemini end-to-end runs; repeated compilation against frozen inputs; stability, latency, usage and cost assessment; independent audit of retained artifacts.

**Not claimed:** universal AI engine coverage, production multi-tenant scale, guaranteed visibility lift, validated customer ROI or general live monitoring.

## An example reviewer journey

1. See an illustrative brand-query observation with explicit provider/surface context.
2. Inspect which text was observed and which metric was derived.
3. Review the source and policy references required for reconstruction.
4. See a missing-evidence or unsupported-claim case fail safely.
5. Understand whether the example is a fixture, preview or independently audited live run.

*This is the intended review flow, not a claim of a completed public live demo.*

## Roadmap

**Now:** close the live Stage C evidence gate and package one defensible Evidence Pack.  
**Next:** discovery with agencies, bounded real-brand reporting pilots, validate willingness to pay for evidence quality.  
**Later:** multi-provider expansion, change tracking, APIs and agency workflow tooling only after technical and commercial proof.

**My contribution:** product framing, architecture/governance contracts, evaluation and delivery orchestration, technical-commercial translation and evidence-led review.

Source code and operational documentation remain private; this case study intentionally excludes proprietary prompts, scoring rules, keys, private customer information and unverified outcomes.

[Back to portfolio](../README.md)
