# persona2_cs_data_structures.pdf — PLACEHOLDER

**Replace this `.md` with the actual `.pdf` when sourced.**

## Requirements

| Field | Spec |
|---|---|
| Persona | 2 — Computer Science (Prof. James Chen, *CS 245: Data Structures*) |
| Subject matter | Chapter on a core data structure: sorting, hashing, trees, graphs, or heaps |
| Length | 20–30 pages |
| Reading level | Undergraduate CS (sophomore/junior) |
| Must contain | Algorithm pseudocode, complexity analysis, proofs or derivations, example walkthroughs |

## Why this is a tricky persona

Persona 2 (Prof. Chen) is the most likely **skeptic-by-expertise** — he already uses Copilot, suspects this is too basic. The sample must be substantive enough that the grounded vs. vanilla comparison reveals a real difference. Generic "intro to programming" PDFs won't move him.

## Suggested sourcing

- **"Open Data Structures"** by Pat Morin — opendatastructures.org (CC-BY)
- **MIT OpenCourseWare** — 6.006 lecture notes
- **LibreTexts Computer Science**
- **"Algorithms"** by Jeff Erickson — jeffe.cs.illinois.edu (CC-BY-NC-SA, check compatibility)

## Demo questions the document should answer well

1. *"What are the key concepts a student should learn from this chapter?"*
2. *"Explain the complexity analysis presented here in plain language."*
3. *"Generate 5 quiz questions at undergraduate level testing the algorithms in this chapter."*

## Quality check

Before staging:
- [ ] Loads in `PyPDFLoader` without errors (math notation can break extraction — verify text is readable)
- [ ] AI explains the algorithm correctly when grounded
- [ ] Vanilla LLM produces plausible-but-wrong details that the grounded version corrects
