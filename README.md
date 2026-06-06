# AI Governance in Brazilian Universities
## Mapping Institutional Policies on Artificial Intelligence Use in Teaching and Research (2022–2026)

## Overview

The rapid diffusion of generative AI tools — accelerated by the public release of ChatGPT in late 2022 — has forced higher education institutions worldwide to confront an unprecedented normative challenge: how to regulate a technology that is simultaneously a research object, a pedagogical tool, and a threat to academic integrity. In Brazil, this challenge intersects with a fragmented institutional landscape of over 2,000 higher education institutions spanning public federal and state universities, private institutions, and specialized centers, each with distinct governance structures, research cultures, and regulatory capacities.

This project maps, collects, and analyzes the documents issued by Brazilian universities and federal bodies regarding the use of artificial intelligence in teaching and research. It covers the period from 2022 to the present, capturing the full arc from the first pioneering institutional responses to the consolidation of normative frameworks at the federal level. The corpus comprises 27 documents from 20 institutions across all regions of Brazil, including federal and state universities, private institutions, and federal bodies (CNPq and MEC). The levantamento is ongoing; the dataset is updated as new documents are identified.

---

## Research Questions

*Research questions are being developed through document analysis and will be formalized in a subsequent phase of the project. The questions below are preliminary and subject to revision.*

- What types of normative instruments have Brazilian universities adopted to regulate AI use, and how do they differ in binding force and scope?
- What is the geographic and institutional distribution of AI governance documents, and what does the absence of documents in certain regions reveal?
- What are the dominant thematic axes across Brazilian university AI policies (academic integrity, data protection, transparency, pedagogical use)?
- How do institutional documents relate to the national frameworks produced by CNPq and MEC?
- What distinguishes institutions that have produced binding resolutions from those that remain at the stage of recommendations or ongoing deliberation?

---

## Data Sources

### Institutional documents on AI use — universities and federal bodies (27 documents)

**How it was obtained:**
The corpus was assembled through systematic web searches targeting institutional websites, official gazettes, and document repositories. The primary aggregator used as a starting point was the *Understanding AI* project at IEA/USP (`understandingai.iea.usp.br`), which maintains a curated list of AI guidelines in Brazilian and international higher education. This was supplemented by direct searches on institutional websites for universities not covered by that repository, with particular attention to institutions in the North and Center-West regions.

**Nature of the corpus:**
This is not a statistical sample — it is an exhaustive documentary corpus bounded by public availability. Every document included was identified through active search; the corpus does not claim to capture all existing documents, only all publicly available documents identified through the search protocol described above. The absence of documents from certain institutions (notably in the North and Center-West) is itself an analytically significant finding: it may reflect the absence of formal policies, the existence of policies not yet made publicly available, or gaps in institutional communication infrastructure. This distinction cannot be resolved from the documents alone.

The corpus includes documents with varying normative status: binding resolutions approved by university councils, non-binding recommendations and guidelines, sectoral directives issued by individual faculties, portarias issued by pro-rectorates, and documents from institutions currently in the process of drafting formal policies. This heterogeneity is a feature of the corpus, not a limitation to be corrected — it reflects the actual state of AI governance in Brazilian higher education.

**Access restrictions:**
All documents in this corpus are publicly available on institutional websites. No restricted or confidential materials were used. Full metadata, including direct links to source documents, is available in `data/raw/levantamento_ia_universidades_brasileiras.csv`. PDF files downloaded for analysis are not versioned in this repository due to file size; the download notebook reproduces the collection from the original sources.

---

## Methodological Note

This project follows a documentary research methodology standard in historical and policy analysis. The corpus is treated as a set of primary sources to be read for their explicit content, their omissions, and their relationship to broader normative developments at the national and international level.

The levantamento phase (document identification and metadata collection) relied on iterative web search, with each search round targeting institutions not covered by previous rounds. Search queries were documented in the project log. The criterion for inclusion was the existence of an institutional document — of any normative status — explicitly addressing AI use in teaching, research, or extension activities, issued after January 2022.

Institutions for which no document was found are recorded as absences, not excluded from the analysis. The distinction between institutions that have no policy, institutions whose policy is not publicly available, and institutions whose policy exists but was not identified by the search protocol is methodologically significant and is discussed in the RESEARCH_LOG.

Full methodological detail, including search queries, inclusion/exclusion decisions, and analytical choices, is documented in `RESEARCH_LOG.md`.

---

## Repository Structure

```
ai-governance-brazilian-universities/
├── README.md
├── RESEARCH_LOG.md
├── config.yaml
├── requirements.txt
├── data/
│   ├── raw/
│   │   └── levantamento_ia_universidades_brasileiras.csv   # corpus metadata
│   └── processed/
│       └── documentos/     # downloaded PDFs (not versioned — see .gitignore)
├── notebooks/
│   └── download_documentos_ia.ipynb    # reproduces document collection
├── scripts/
└── outputs/
```

---

## Key Findings (Preliminary)

- The normative wave is recent and accelerating: virtually no Brazilian university had a formal AI document before 2024; the largest concentration of publications falls in 2025, with federal-level frameworks (CNPq, MEC) emerging only in 2026.
- There is a sharp geographic asymmetry: the South and Southeast account for the majority of documents; the North has no institution with a published institutional policy, despite active investment in AI degree programs.
- Normative instruments vary widely in binding force — from resolutions approved by university councils (UNESP, UNICAMP, UFDPar) to non-binding recommendations — and this variation is not correlated with institutional size or prestige.
- Several major federal universities (UnB, UFSC, UFRGS) are in active deliberation but have not yet produced binding documents, suggesting that the normative landscape is still in formation.
- PUC-SP's *Manual Ético* (TECCOGS, 2023) is the earliest document identified and is frequently cited by subsequent institutional documents, functioning as a reference text for the field.
- The dominant thematic axes across documents are academic integrity and plagiarism, mandatory disclosure of AI use, and data protection (LGPD compliance) — with significant variation in how each is operationalized.

---

## Tools and Libraries

- Python 3.x — `pandas`, `requests`, `tqdm`, `pathlib`
- Jupyter Notebook
- Git / GitHub

---

## Related Work

- Understanding AI — IEA/USP: curated repository of AI guidelines in higher education (`understandingai.iea.usp.br`)
- ANDIFES: *Diretrizes para o Uso de IA nas IFES* (2025) — collective guidelines for federal universities
- Sampaio, R.C.; Sabbatini, M.; Limongi, R. *Diretrizes para o uso ético e responsável da Inteligência Artificial Generativa: um guia prático para pesquisadores*. São Paulo: Intercom, 2024
- UNESCO: *Recommendation on the Ethics of Artificial Intelligence* (2021)
- MEC: *Referencial para o uso e desenvolvimento responsáveis de IA na educação* (2026)

---

## Data Availability Statement

All data produced by this project is publicly available in this repository. The file `data/raw/levantamento_ia_universidades_brasileiras.csv` contains full metadata for all 27 documents in the corpus, including direct links to source documents on institutional websites. No personally identifiable information was collected or processed. The source documents are institutional policy texts issued by public and private universities and federal bodies; they are public records available on institutional websites and are not reproduced in this repository. The download notebook (`notebooks/download_documentos_ia.ipynb`) allows full reproduction of the document collection from original sources.

---

## Author

Gabriel Fonteles — Doutor em História pela PUC-SP
[Afiliação institucional]
[Contato ou perfil acadêmico]

---

## License

Code: MIT License
Data: Creative Commons CC BY 4.0 — metadata and analytical outputs are freely reusable with attribution. Source documents are subject to the terms of their original publishers.
