# Faculty AI Seminar — Lab 2

**Build a Discipline-Specific AI Teaching Assistant**

This repo contains everything you need to run Lab 2 of the 1-day Faculty AI Seminar. By the end of this 90-minute lab, you'll have a working AI tutor grounded in *your discipline's* content — quiz questions, study guides, or grading rubrics drawn from material you upload.

## Quick start (in SageMaker Studio)

1. **Open SageMaker Studio** in JupyterLab mode (URL provided by your seminar instructor)
2. **Clone this repo** — click the Git icon in the left sidebar → **Clone a Repository** → paste this repo's URL
3. **Open `discipline-assistant.ipynb`**
4. **Run cells top to bottom** — the notebook walks you through everything
5. **Work through it during the 1:30–3:00 PM lab block**

## What's in this repo

```
faculty-ai-seminar-lab2/
├── README.md                      ← you are here
├── requirements.txt               ← Python package versions
├── discipline-assistant.ipynb     ← the lab notebook
├── data/                          ← 6 sample PDFs (one per persona)
│   ├── README.md
│   └── persona{1..6}_*.pdf
└── instructor/                    ← run-of-show and setup docs
    ├── SEMINAR_PLAN.md
    ├── INSTRUCTOR_CHEATSHEET.md
    └── PREFLIGHT_CHECKLIST.md
```

## What you need

- AWS account with **Amazon Bedrock** model access for:
  - `amazon.nova-lite-v1:0`
  - `amazon.nova-2-multimodal-embeddings-v1:0`
  - `mistral.mixtral-8x7b-instruct-v0:1`
- **SageMaker Studio** with a Python 3 (Data Science) kernel, `ml.t3.medium` or larger
- Region: `us-east-1`

If you don't have these, contact your seminar instructor — they'll get you set up.

## The 6 personas

| # | Persona | Sample PDF |
|---|---|---|
| 1 | Dentistry | `data/persona1_dentistry_perio_case.pdf` |
| 2 | Computer Science | `data/persona2_cs_data_structures.pdf` |
| 3 | English Literature | `data/persona3_english_victorian_essay.pdf` |
| 4 | Nursing | `data/persona4_nursing_pharmacology.pdf` |
| 5 | Business / MBA | `data/persona5_business_leadership_case.pdf` |
| 6 | Biology | `data/persona6_biology_lab_protocol.pdf` |

The notebook defaults to Persona 1 (Dentistry). Change the `pdf_path` in Section 3.1 to match your persona.

## After the seminar

The notebook is yours to customize. Three things to change to adapt this for your own course:

1. **Swap the document** — point `pdf_path` at your real syllabus, lecture notes, or textbook
2. **Edit the prompt templates** — change the quiz style, rubric criteria, study-guide format to match your teaching
3. **Add more documents** — load multiple PDFs into one vector store for whole-semester coverage

See the "What to try next (Monday morning)" section at the bottom of the notebook.

## Troubleshooting

- **`AccessDeniedException` on model invoke** — Bedrock model access not enabled in your account. Check the AWS Bedrock console → Model access.
- **Embedding cell hangs > 90 sec** — Your PDF is too large (50-page cap recommended). Swap to a smaller sample.
- **`Could not load PDF`** — PDF is scanned (image-only), not text. The PDF loader can't read scanned documents.
- **Kernel disconnected** — Restart the kernel and re-run from Section 1.2.

For more, see `instructor/INSTRUCTOR_CHEATSHEET.md`.

## Built on

This lab adapts components from the [AWS MLU EEP Generative AI](https://github.com/aws-samples/aws-mlu-eep-generative-ai) curriculum — specifically the RAG patterns from Module 3 Lab 3a.
