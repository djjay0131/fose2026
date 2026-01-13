# Phases: FOSE 2026 Paper Writing Coordination Hub

**Last Updated:** 2026-01-12 (Phase 1-2 COMPLETE)

## Purpose

This file serves as the **coordination hub** linking the memory-bank documentation to the actual paper writing work. It tracks the lifecycle of each writing phase, maintains links to section drafts, and coordinates multi-session work.

## Phase Status Legend

- **NOT_STARTED**: Phase not yet begun
- **IN_PROGRESS**: Active work on this phase
- **BLOCKED**: Waiting on dependency or decision
- **REVIEW**: Draft complete, under review
- **COMPLETE**: Finalized and integrated
- **DEFERRED**: Postponed to later

---

## Phase Registry

### Phase 1: Foundation and Survey Analysis ⚡ PRIORITY

**Status:** COMPLETE ✓
**Started:** 2026-01-12
**Completed:** 2026-01-12

**Description:**
Analyze FOSE pre-survey data and draft Section 3 (Survey Synthesis) establishing empirical foundation for structural diagnosis.

**Key Tasks:**
- [x] Analyze survey XLSX and PPTX data files
- [x] Extract demographics (experience, productivity, geography)
- [x] Create survey summary table/figure (included in Section 3)
- [x] Draft `sections/03_survey.tex`
- [x] Validate survey claims against raw data

**Files:**
- Input: `files/icse_2026_fose_pre-survey_completed_raw_data copy.xlsx`
- Input: `files/icse_2026_fose_pre-survey_basic_data.pptx`
- Analysis: `memory-bank/survey-analysis.md`
- Output: `sections/03_survey.tex` ✓ COMPLETE

**Dependencies:**
- None (can start immediately)

**Completion Notes:**
- Survey analysis complete with 280 responses
- Key findings: 57.1% experienced (11+ years), 44.3% productive (11+ papers/3yr), 6 regions
- Demographics table included in Section 3
- Core argument established: expertise/participation NOT bottleneck → STRUCTURAL problem
- Section 3 draft complete with proper FOSE tone (descriptive, not overclaiming)

---

### Phase 2: Structural Diagnosis ⚡ PRIORITY

**Status:** COMPLETE ✓
**Started:** 2026-01-12
**Completed:** 2026-01-12

**Description:**
Draft Section 4 (Breakdown Diagnosis) articulating four structural barriers to knowledge accumulation.

**Key Tasks:**
- [x] Draft breakdown 1: Papers as isolated knowledge units
- [x] Draft breakdown 2: Loss of context and provenance
- [x] Draft breakdown 3: Claims evolve without tracking
- [x] Draft breakdown 4: Incentives favor novelty over accumulation
- [x] Find concrete examples for each breakdown
- [x] Connect breakdowns to survey findings
- [x] Complete `sections/04_breakdown.tex`

**Files:**
- Input: `sections/03_survey.tex` (for connections)
- Output: `sections/04_breakdown.tex` ✓ COMPLETE

**Dependencies:**
- Ideally follows Phase 1 (survey synthesis) - ✓ MET

**Completion Notes:**
- All four structural breakdowns articulated with concrete examples
- Balanced critique with constructiveness; maintained reflective tone
- Connected to survey findings (experienced/productive community → structural not individual)
- Added interconnected challenges subsection showing how breakdowns reinforce each other
- Clear transition to Section 5 (Principles) established

---

### Phase 3: Principles for Future Artifacts ⚡ PRIORITY

**Status:** NOT_STARTED
**Started:** -
**Completed:** -

**Description:**
Draft Section 5 (Principles) articulating actionable principles for future research artifacts without over-prescribing tools.

**Key Tasks:**
- [ ] Draft principle 1: Structured and interpretable
- [ ] Draft principle 2: Inspectable and provenance-aware
- [ ] Draft principle 3: Long-lived and reusable
- [ ] Draft principle 4: Governed with human oversight
- [ ] Provide instantiation examples (lightweight, not prescriptive)
- [ ] Map principles back to diagnosed breakdowns
- [ ] Complete `sections/05_principles.tex`

**Files:**
- Input: `sections/04_breakdown.tex` (for connections)
- Output: `sections/05_principles.tex`

**Dependencies:**
- Ideally follows Phase 2 (breakdown diagnosis)
- Can draft in parallel with earlier phases

**Notes:**
- Principles not tools
- Examples illustrative not endorsements
- Connect each principle to specific breakdown
- Maintain FOSE-appropriate level of abstraction

---

### Phase 4: Framing and Context

**Status:** NOT_STARTED
**Started:** -
**Completed:** -

**Description:**
Draft introduction, background/related work, and refine abstract to frame the paper appropriately.

**Key Tasks:**
- [ ] Draft `sections/01_introduction.tex`
  - Hook: Productivity vs. progress tension
  - Contributions and paper structure
  - Explicit framing as diagnosis + principles
- [ ] Draft `sections/02_background.tex`
  - Knowledge accumulation in SE
  - Meta-research and reproducibility
  - Knowledge graphs in science
  - Research infrastructure efforts
- [ ] Refine abstract in `main.tex`
  - Core tension
  - Survey role
  - Diagnosis and principles summary
  - Contribution framing

**Files:**
- Output: `sections/01_introduction.tex`
- Output: `sections/02_background.tex`
- Updated: `main.tex` (abstract)

**Dependencies:**
- Should follow Phases 1-3 to ensure accurate framing
- Background can be drafted earlier if needed

**Notes:**
- Position as synthesis not novelty
- Avoid appearing naive about related work
- Introduction should hook FOSE audience

---

### Phase 5: Implications and Limitations

**Status:** NOT_STARTED
**Started:** -
**Completed:** -

**Description:**
Draft implications, limitations, and conclusion sections.

**Key Tasks:**
- [ ] Draft `sections/06_implications.tex`
  - For research practice
  - For publication and review
  - For community infrastructure
  - For FOSE as experimentation venue
- [ ] Draft `sections/07_limitations.tex`
  - Survey limitations
  - Principle generality tradeoffs
  - Feasibility and adoption challenges
  - Open questions
- [ ] Draft `sections/08_conclusion.tex`
  - Restate core argument
  - Emphasize call-to-action
  - Point to next steps

**Files:**
- Input: All prior sections
- Output: `sections/06_implications.tex`
- Output: `sections/07_limitations.tex`
- Output: `sections/08_conclusion.tex`

**Dependencies:**
- Requires Phases 1-4 complete or nearly complete

**Notes:**
- Implications should be concrete and actionable
- Limitations demonstrate reflexivity and humility
- Conclusion reinforces FOSE agenda-setting tone

---

### Phase 6: Integration and Polish

**Status:** IN_PROGRESS (LaTeX compilation pending user installation)
**Started:** 2026-01-12
**Completed:** -

**Description:**
Integrate all sections, ensure narrative coherence, and polish for submission.

**Key Tasks:**
- [x] Integrate all sections into `main.tex`
- [x] Check narrative flow between sections
- [x] Ensure consistent terminology throughout
- [x] Add CCS concepts
- [ ] Test LaTeX compilation (BLOCKED - requires MacTeX/BasicTeX installation)
- [x] Replace bibliography placeholders with actual citations
- [x] Check ACM formatting compliance
- [ ] Final proofread for clarity and grammar

**Files:**
- Input: All `sections/*.tex` files
- Updated: `main.tex`
- Validated: `bibliography.bib`, `software.bib`

**Dependencies:**
- Requires all section drafts complete

**Notes:**
- Use ACM CCS tool: https://dl.acm.org/ccs
- Verify anonymous submission format
- Check page limits

---

### Phase 7: Submission Preparation

**Status:** NOT_STARTED
**Started:** -
**Completed:** -

**Description:**
Final compilation, validation, and submission.

**Key Tasks:**
- [ ] Final compile: `pdflatex → bibtex → pdflatex × 2`
- [ ] Verify anonymous submission format
- [ ] Check page limits
- [ ] Validate bibliography formatting
- [ ] Prepare submission metadata
- [ ] Submit through ICSE 2026 conference system

**Files:**
- Output: `main.pdf` (final)
- Submission package: LaTeX sources + PDF

**Dependencies:**
- Requires Phase 6 complete

**Notes:**
- Keep backup of final submission package
- Note submission confirmation number
- Archive submitted version

---

## Cross-References

### Memory Bank ↔ Paper Sections

| Memory Bank File | Related Paper Sections |
|-----------------|------------------------|
| [projectbrief.md](projectbrief.md) | Abstract, Introduction |
| [productContext.md](productContext.md) | Introduction, Implications |
| [systemPatterns.md](systemPatterns.md) | All sections (structure guide) |
| [techContext.md](techContext.md) | Build and formatting |
| [activeContext.md](activeContext.md) | Current focus |
| [progress.md](progress.md) | Completion tracking |

### Section Dependencies

```
01_introduction.tex → Requires abstract, survey, breakdown, principles
02_background.tex → Independent (can draft early)
03_survey.tex → Independent (PRIORITY 1)
04_breakdown.tex → Depends on survey synthesis (PRIORITY 2)
05_principles.tex → Depends on breakdown (PRIORITY 3)
06_implications.tex → Depends on principles
07_limitations.tex → Depends on all prior sections
08_conclusion.tex → Depends on all prior sections
```

### Data ↔ Sections

| Data File | Used In |
|-----------|---------|
| `icse_2026_fose_pre-survey_completed_raw_data.xlsx` | Section 3 |
| `icse_2026_fose_pre-survey_basic_data.pptx` | Section 3 |
| Survey demographics table/figure | Section 3 |

---

## Agent Coordination Protocols

### Starting a New Phase

1. Update phase status to `IN_PROGRESS`
2. Update `activeContext.md` with current focus
3. Review dependencies and input files
4. Execute phase tasks
5. Update `progress.md` as tasks complete

### Completing a Phase

1. Mark all phase tasks complete
2. Update phase status to `REVIEW` or `COMPLETE`
3. Update `progress.md` with completion date
4. Update `activeContext.md` with learnings/decisions
5. Identify next phase to start

### Handling Blockers

1. Update phase status to `BLOCKED`
2. Document blocker in phase notes
3. Update `activeContext.md` with open question
4. Identify alternative phase to work on
5. Resolve blocker and update status

### Multi-Session Work

**End of Session:**
1. Update phase status and notes
2. Update `activeContext.md` with current state
3. Note any decisions or learnings
4. Mark completed tasks in phase checklist
5. Document next steps

**Start of Session:**
1. Read ALL memory-bank files
2. Check `phases.md` for current phase status
3. Review `activeContext.md` for recent context
4. Continue work on in-progress phases

---

## Archive Policy

### When to Archive

- Old section drafts when major revisions complete
- Decision logs from `activeContext.md` when phase complete
- Data analysis notes after Section 3 complete

### Archive Structure

```
memory-bank/archive/
├── decisions/           # Archived decision logs
├── drafts/             # Superseded section drafts
└── data-analysis/      # Survey analysis working notes
```

### Archive Process

1. Move archived content to appropriate archive subdirectory
2. Add date prefix to filename: `YYYY-MM-DD_filename.md`
3. Update cross-references in active files
4. Document archival in `progress.md`

---

## Status Summary

**Current Phase:** Phase 1 (Foundation and Survey Analysis) - Priority
**Overall Progress:** 0% (0/7 phases complete)
**Active Files:** None yet
**Blockers:** None

**Next Actions:**
1. Start Phase 1: Analyze survey data
2. Draft Section 3: Survey synthesis
3. Validate survey claims

---

**Remember:** This phases.md file is your coordination hub. Update it frequently, use it to track progress, and maintain accurate status for all phases.
