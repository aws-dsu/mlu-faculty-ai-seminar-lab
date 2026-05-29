# persona1_dentistry_perio_case.pdf — PLACEHOLDER

**Replace this `.md` with the actual `.pdf` when sourced.**

## Requirements

| Field | Spec |
|---|---|
| Persona | 1 — Dentistry (Dr. Maya Patel, *Periodontics II*) |
| Subject matter | Clinical periodontal case study OR open-access dental chapter on perio classification/diagnosis |
| Length | 15–25 pages |
| Reading level | DDS student (clinical professional) |
| Must contain | Real clinical detail — probing depths, bleeding scores, radiographic findings, diagnosis reasoning |

## Why this persona leads the demo

Persona 1 is the instructor's go-to demo sample (per `SEMINAR_PLAN.md`). Clinical reasoning creates the strongest "if AI can do this, it can do my field" momentum in a mixed-discipline room. **The CS prof watching a dental case being analyzed is more persuasive than another CS demo.**

## Suggested sourcing

- PubMed Central open-access journal articles (perio case reports)
- LibreTexts Dental Hygiene / Periodontics
- 2018 AAP/EFP classification reference materials (verify open licensing)

## Demo questions the document should answer well

The instructor will ask these live during the Part 3 walkthrough. Pick a document that handles all three:

1. *"What are the key concepts a periodontics student should learn from this material?"*
2. *"Given the clinical findings described here, what's the staging and grading?"*
3. *"Generate 3 case-based discussion questions for tomorrow's seminar."*

## Quality check

Before staging:
- [ ] Loads in `PyPDFLoader` without errors
- [ ] AI produces a substantive answer to all 3 demo questions above
- [ ] Grounded answer noticeably more accurate than vanilla LLM answer
