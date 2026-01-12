# ICSE 2026 FOSE Paper — Context & Design Corpus

## 1. Goal & Venue

- **Target venue:** ICSE 2026 — *Future of Software Engineering (FOSE)*
- **Paper type:** Community-informed, evidence-backed position / perspective paper
- **Primary goal:** Argue that software engineering research productivity is high, but cumulative knowledge progress is structurally limited, and that the future of SE requires rethinking research artifacts and infrastructure.

---

## 2. Chosen Paper Angle

### Working Title
**From Papers to Progress: Rethinking Knowledge Accumulation in Software Engineering**

### Core Thesis
Despite unprecedented research output and senior participation, the software engineering community lacks effective mechanisms for cumulative, interpretable, and reusable knowledge progression.

### Framing Constraints
- Not a tooling paper
- Not a single-solution proposal
- Not technology-prescriptive
- FOSE-style reflective and agenda-setting
- Survey data used to reveal structural symptoms, not preferences

---

## 3. Data Source & Role

### Data
- ICSE 2026 FOSE pre-survey
  - Raw data: `icse_2026_fose_pre-survey_completed_raw_data.xlsx`
  - Summary slides: `icse_2026_fose_pre-survey_basic_data.pptx`

### What the Data Establishes
- Respondents are:
  - Highly experienced (often 10+ years in SE research)
  - Highly productive (multiple submissions in recent years)
  - Globally distributed
- Therefore:
  - Expertise and participation are not the bottleneck
  - Knowledge accumulation issues are structural

### How the Data Is Used
- High-level descriptive evidence only
- No heavy statistics
- Used to justify urgency and legitimacy of the argument

---

## 4. Central Argument

### Diagnosis
- Research output continues to grow
- Knowledge remains fragmented
- Claims, evidence, and context are weakly linked
- Rediscovery and reinterpretation costs remain high

### Structural Breakdowns
1. Papers as isolated knowledge units
2. Loss of context and provenance over time
3. Lack of mechanisms for tracking evolving claims
4. Incentive structures that reward novelty over accumulation

### Proposed Shift (Principles)
- Move from documents → structured research objects
- Emphasize:
  - Interpretability
  - Inspectability
  - Provenance
  - Long-lived knowledge substrates
- Tools (e.g., knowledge graphs, AI systems) are examples, not contributions

---

## 5. Contributions

1. Community-informed diagnosis of accumulation challenges
2. Synthesis of structural barriers to progress
3. Principles for future research artifacts
4. Implications for:
   - Research practice
   - Publication and review
   - Community infrastructure
   - FOSE as an experimentation venue

---

## 6. Abstract (Working Version)

Software engineering research has experienced sustained growth in both output and participation over the past decades. Yet concerns persist about the field’s ability to accumulate, integrate, and reuse knowledge in ways that support long-term progress. To better understand how the community itself perceives these challenges, we analyze responses from the ICSE 2026 Future of Software Engineering pre-survey, which captures perspectives from a globally distributed and highly experienced set of researchers. Our analysis reveals a tension between increasing research productivity and the limited mechanisms available for synthesizing results, tracking evolving claims, and supporting cumulative understanding over time. Building on these observations, we argue that future progress in software engineering will require rethinking the dominant research artifacts and infrastructures that shape how knowledge is produced, evaluated, and reused. We outline a set of principles for more cumulative, interpretable, and provenance-aware research artifacts, and discuss their implications for the future of software engineering research and community practice.

---

## 7. Paper Outline

1. Introduction  
2. Background and Related Perspectives  
3. Community Signals from the ICSE 2026 FOSE Pre-Survey  
4. Where Knowledge Accumulation Breaks Down  
5. Rethinking Research Artifacts for Cumulative Progress  
6. Implications for the Future of Software Engineering  
7. Limitations and Open Questions  
8. Conclusion

---

## 8. LaTeX / ACM Decisions

- ACM `acmart` template (`sigconf`)
- Anonymous authorship
- Minimal `main.tex`
- Sections split into `sections/*.tex`
- CCS concepts and rights blocks deferred

---

## 9. Reviewer Risk Controls

Explicitly avoided:
- Over-prescription of tools or platforms
- Heavy formalism
- Empirical overclaiming
- Self-promotional framing

---

## 10. Next Execution Steps

1. Draft `sections/03_survey.tex`
2. Draft `sections/04_breakdown.tex`
3. Refine abstract tone
4. Optional: light instantiation references later
