# System Patterns: Paper Structure and Argumentation

**Last Updated:** 2026-01-12

## Paper Architecture

### Document Structure

```
fose2026/
├── main.tex                 # Main LaTeX entry point
├── sections/               # Section files
│   ├── 01_introduction.tex
│   ├── 02_background.tex
│   ├── 03_survey.tex       # Survey synthesis (PRIORITY 1)
│   ├── 04_breakdown.tex    # Accumulation failures (PRIORITY 2)
│   ├── 05_principles.tex   # Future artifacts (PRIORITY 3)
│   ├── 06_implications.tex
│   ├── 07_limitations.tex
│   └── 08_conclusion.tex
├── bibliography.bib        # Main bibliography
├── software.bib           # Software/tool references
└── acmart.cls             # ACM template class
```

### Section Dependencies

```
Introduction (1)
    │
    ├─→ Background (2)
    │       │
    │       └─→ Survey Synthesis (3)
    │               │
    │               └─→ Breakdown Diagnosis (4)
    │                       │
    │                       └─→ Principles (5)
    │                               │
    │                               └─→ Implications (6)
    │                                       │
    │                                       ├─→ Limitations (7)
    │                                       │
    │                                       └─→ Conclusion (8)
```

## Implementation Phases

### Phase 1: Foundation and Survey Analysis (PRIORITY)

**Goal:** Establish empirical foundation using FOSE pre-survey data

**Tasks:**
1. Analyze survey data (XLSX + PPTX)
   - Extract key demographics (experience, productivity, geography)
   - Identify quotes or patterns relevant to accumulation challenges
   - Prepare high-level descriptive statistics
2. Draft Section 3: Survey Synthesis
   - Frame survey purpose and methodology
   - Present demographic findings
   - Establish "expertise is not the bottleneck" argument
   - Connect survey findings to structural diagnosis
3. Create survey summary table or figure
4. Validate survey claims against raw data

**Deliverables:**
- [ ] Survey data analysis notes
- [ ] Section 3 draft (`sections/03_survey.tex`)
- [ ] Survey summary figure/table (if needed)

---

### Phase 2: Structural Diagnosis (PRIORITY)

**Goal:** Articulate where and why knowledge accumulation breaks down

**Tasks:**
1. Draft Section 4: Breakdown Diagnosis
   - **Breakdown 1:** Papers as isolated knowledge units
     - Claims are embedded in prose
     - Evidence is not structured
     - Results are not directly comparable
   - **Breakdown 2:** Loss of context and provenance
     - Motivation and assumptions fade
     - Methodological decisions not preserved
     - Evolution of ideas not tracked
   - **Breakdown 3:** Claims evolve without tracking
     - Contradictions go unnoticed
     - Refinements are implicit
     - Relationships between claims unclear
   - **Breakdown 4:** Incentive structures favor novelty
     - Publication rewards new contributions
     - Replication and consolidation undervalued
     - Infrastructure work marginalized
2. Find concrete examples for each breakdown
3. Connect breakdowns back to survey findings
4. Ensure diagnosis avoids sounding purely negative

**Deliverables:**
- [ ] Section 4 draft (`sections/04_breakdown.tex`)
- [ ] Example vignettes or scenarios
- [ ] Explicit connections to survey evidence

---

### Phase 3: Principles for Future Artifacts (PRIORITY)

**Goal:** Articulate actionable principles without over-prescribing tools

**Tasks:**
1. Draft Section 5: Principles for Future Research Artifacts
   - **Principle 1:** Structured and interpretable
     - Claims, evidence, and context as first-class entities
     - Machine-readable representations
     - Human-interpretable interfaces
   - **Principle 2:** Inspectable and provenance-aware
     - Full traceability from claim to source
     - Decision rationales preserved
     - Evolution tracked over time
   - **Principle 3:** Long-lived and reusable
     - Substrates outlive individual papers
     - Results can be directly reused
     - Integration over reinvention
   - **Principle 4:** Governed with human oversight
     - Community validation mechanisms
     - Quality control processes
     - Ethical and social considerations
2. Provide concrete examples of each principle
3. Avoid prescribing specific technologies
4. Connect principles back to diagnosed breakdowns

**Deliverables:**
- [ ] Section 5 draft (`sections/05_principles.tex`)
- [ ] Principle-breakdown mapping
- [ ] Instantiation examples (lightweight, not prescriptive)

---

### Phase 4: Framing and Context

**Goal:** Situate paper within SE and broader research context

**Tasks:**
1. Draft Section 1: Introduction
   - Hook: Productivity vs. progress tension
   - Motivating scenario or observation
   - Paper contributions and structure
   - Explicit framing as diagnosis + principles
2. Draft Section 2: Background and Related Work
   - Knowledge accumulation challenges in SE
   - Meta-research and reproducibility movements
   - Knowledge graphs in science (ORKG, AI-KG, etc.)
   - Research infrastructure efforts
   - Position paper as synthesis, not novelty claim
3. Refine abstract
   - Core tension
   - Survey role
   - Diagnosis summary
   - Principles summary
   - Contribution framing

**Deliverables:**
- [ ] Section 1 draft (`sections/01_introduction.tex`)
- [ ] Section 2 draft (`sections/02_background.tex`)
- [ ] Refined abstract in `main.tex`

---

### Phase 5: Implications and Limitations

**Goal:** Discuss practical consequences and acknowledge constraints

**Tasks:**
1. Draft Section 6: Implications
   - For research practice (how researchers work)
   - For publication and review (how papers are evaluated)
   - For community infrastructure (what platforms are needed)
   - For FOSE as experimentation venue
2. Draft Section 7: Limitations and Open Questions
   - Survey limitations (scope, representativeness)
   - Principle generality vs. specificity tradeoffs
   - Feasibility and adoption challenges
   - Open questions for future work
3. Draft Section 8: Conclusion
   - Restate core argument
   - Emphasize call-to-action
   - Point to concrete next steps

**Deliverables:**
- [ ] Section 6 draft (`sections/06_implications.tex`)
- [ ] Section 7 draft (`sections/07_limitations.tex`)
- [ ] Section 8 draft (`sections/08_conclusion.tex`)

---

### Phase 6: Integration and Polish

**Goal:** Ensure coherent narrative and meet formatting requirements

**Tasks:**
1. Integrate all sections into `main.tex`
2. Check narrative flow between sections
3. Ensure consistent terminology
4. Add CCS concepts
5. Configure rights management block
6. Verify bibliography completeness
7. Check ACM formatting compliance
8. Proofread for clarity and grammar

**Deliverables:**
- [ ] Fully integrated `main.tex`
- [ ] Compiled PDF without errors
- [ ] Final proofreading complete

---

### Phase 7: Submission Preparation

**Goal:** Prepare final submission package

**Tasks:**
1. Final compile and PDF generation
2. Verify anonymous submission format
3. Check page limits
4. Validate bibliography formatting
5. Prepare submission metadata
6. Submit through conference system

**Deliverables:**
- [ ] Final PDF
- [ ] Submission confirmation

---

## Argumentation Patterns

### Core Narrative Arc

1. **Hook** (Introduction): SE is productive but progress is limited
2. **Evidence** (Survey): Community is experienced and productive
3. **Implication**: Therefore, problem is structural, not individual
4. **Diagnosis** (Breakdown): Four structural barriers identified
5. **Prescription** (Principles): Four principles for future artifacts
6. **Impact** (Implications): How principles reshape practice
7. **Humility** (Limitations): Acknowledged constraints and open questions
8. **Call-to-Action** (Conclusion): FOSE as venue for experimentation

### Rhetorical Strategies

**Balance Critique with Constructiveness:**
- Diagnosis identifies problems
- Principles offer path forward
- Implications provide concrete guidance
- Avoid purely negative framing

**Ground Claims in Evidence:**
- Survey data establishes community context
- Concrete examples illustrate breakdowns
- Related work shows broader patterns
- Principles connect to diagnosed problems

**Avoid Over-Prescription:**
- Principles, not specific tools
- Examples, not endorsements
- Implications, not mandates
- Open questions, not final answers

**FOSE-Appropriate Tone:**
- Reflective, not prescriptive
- Forward-looking, not backward-blaming
- Community-focused, not individual-focused
- Agenda-setting, not problem-solving

### Key Transitions

**Survey → Diagnosis:**
"Given this experienced and productive community, accumulation challenges must be structural..."

**Diagnosis → Principles:**
"Addressing these structural barriers requires rethinking the fundamental properties of research artifacts..."

**Principles → Implications:**
"Adopting these principles would reshape research practice in several ways..."

**Implications → Limitations:**
"While these principles offer a path forward, important questions remain..."

**Limitations → Conclusion:**
"Despite these open challenges, the need for action is clear. FOSE provides an ideal venue to..."

## Critical Paths and Workflows

### Survey Data Analysis Path
1. Read raw XLSX survey data
2. Extract demographic summaries
3. Identify relevant quotes or patterns
4. Create summary visualization (optional)
5. Draft Section 3 incorporating findings
6. Validate claims against data

### Breakdown Development Path
1. Brainstorm accumulation failure modes
2. Organize into 4 core categories
3. Find concrete examples for each
4. Connect to survey evidence
5. Draft Section 4
6. Review for balance (not too negative)

### Principles Development Path
1. Identify properties addressing each breakdown
2. Cluster into 4 core principles
3. Find instantiation examples (avoid over-prescription)
4. Draft Section 5
5. Review for actionability without specificity

### Integration Path
1. Draft priority sections (3, 4, 5)
2. Draft framing sections (1, 2)
3. Draft implications sections (6, 7, 8)
4. Integrate into `main.tex`
5. Check narrative flow
6. Polish and proofread
7. Submit

## Design Patterns

### Section Structure Pattern
Each section should follow:
1. **Opening paragraph**: What this section does
2. **Body**: Core content organized logically
3. **Closing paragraph**: What this section established + transition

### Principle Structure Pattern
Each principle should include:
1. **Name**: Short, memorable label
2. **Statement**: Clear articulation of the principle
3. **Rationale**: Why this principle matters
4. **Example**: Concrete instantiation (avoid tool evangelism)
5. **Connection**: Link back to diagnosed breakdown

### Example Pattern
When providing examples:
1. Use generic or hypothetical scenarios when possible
2. If referencing specific tools, use multiple to avoid endorsement
3. Frame as "illustrative" not "recommended"
4. Keep examples brief and focused on principle illustration

## Quality Assurance Patterns

### Self-Review Checklist (per section)
- [ ] Clear topic sentences for each paragraph
- [ ] Logical flow between paragraphs
- [ ] Evidence supports claims
- [ ] Tone appropriate for FOSE
- [ ] No over-prescription of tools
- [ ] Terminology consistent with rest of paper
- [ ] Citations complete
- [ ] Transitions to next section clear

### Integration Review Checklist
- [ ] Narrative arc coherent across sections
- [ ] Terminology consistent throughout
- [ ] Survey data used appropriately
- [ ] Principles clearly address diagnosed breakdowns
- [ ] Implications concretely follow from principles
- [ ] Limitations honestly acknowledged
- [ ] Conclusion reinforces call-to-action

### Submission Review Checklist
- [ ] ACM formatting correct
- [ ] Anonymous submission format
- [ ] Bibliography complete
- [ ] CCS concepts added
- [ ] Rights management configured
- [ ] Compiles without errors
- [ ] Within page limits
- [ ] Final proofread complete

---

**Remember:** The paper succeeds through clear diagnosis, principled prescription, and FOSE-appropriate tone. Avoid tool evangelism, maintain evidence grounding, and keep narrative arc coherent.
