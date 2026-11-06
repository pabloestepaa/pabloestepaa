# Hi, I'm Pablo Estepa

**Software Engineer · AI/LLM engineering (RAG, agents, MCP, evals) · Antimicrobial resistance**

I build production software for a living, and I build LLM systems with the same habits: tests,
evals that run in CI, and a deployed demo you can try. My domain is antimicrobial resistance (AMR),
which is also the subject of my bachelor's thesis. Computer Engineering (Computing track) at the
University of Córdoba, Spain.

## What I'm working on

### [amr-research-agent](https://github.com/pabloestepaa/amr-research-agent) · RAG and a tool-calling agent for AMR research
[![CI](https://github.com/pabloestepaa/amr-research-agent/actions/workflows/ci.yml/badge.svg)](https://github.com/pabloestepaa/amr-research-agent/actions/workflows/ci.yml)
[![Live demo](https://img.shields.io/badge/live_demo-Render-46E3B7)](https://amr-research-agent.onrender.com)

Answers questions about AMR with hybrid RAG over ~3,000 PubMed abstracts (Postgres full-text and
pgvector, fused with RRF) and with a tool-calling agent that queries NCBI through amr-mcp, my MCP
server. A PMID only counts as a citation if a tool returned it: no invented PMIDs in 64 evaluated
answers. Evals run at three levels: retrieval in CI (recall@10 0.97), answers with an LLM judge,
and agent trajectories (19/22 tasks fully correct). It runs on free tiers (Render, Neon, Groq).
*Python · FastAPI · PostgreSQL + pgvector · MCP · Groq · Docker · GitHub Actions*

### [amr-mcp](https://github.com/pabloestepaa/amr-mcp) · AMR data for AI assistants
[![PyPI](https://img.shields.io/pypi/v/amr-mcp)](https://pypi.org/project/amr-mcp/)
[![CI](https://github.com/pabloestepaa/amr-mcp/actions/workflows/ci.yml/badge.svg)](https://github.com/pabloestepaa/amr-mcp/actions/workflows/ci.yml)

An [MCP](https://modelcontextprotocol.io) server that lets Claude, Codex or Cursor query antimicrobial resistance data:
the NCBI Reference Gene Catalog behind AMRFinderPlus (~11,500 genes), NCBI E-utilities (sequences, PubMed),
UniProt, and local AMRFinderPlus runs. Public data only, no API keys. It is also the agent's tool server in
amr-research-agent. `pip install amr-mcp`

### [amr-metaheuristics-xai](https://github.com/pabloestepaa/amr-metaheuristics-xai) · Bachelor's thesis: AMR prediction with explainable feature selection
Predicting antibiotic susceptibility in *E. coli* (ampicillin, ciprofloxacin, trimethoprim/sulfamethoxazole)
from genomic data (gene presence/absence and SNPs) with a custom evolutionary metaheuristic for feature selection,
benchmarked against classical baselines with nested cross-validation and statistical tests.
Next phase: explainability, turning the selected features into template-based and LLM-generated explanations.
*Python · scikit-learn · XGBoost · pandas · pytest* (in progress)

### Open source · [nf-core](https://nf-co.re)
Contributing modules to nf-core, the community of bioinformatics pipelines built with Nextflow.
- [`hamronization/resfinder`](https://github.com/nf-core/modules/pull/13565): converts ResFinder results to the hAMRonization AMR reporting standard (in review)
- [Test data](https://github.com/nf-core/test-datasets/pull/2360) for the module in nf-core/test-datasets

### Software Engineer · Azabache Ingeniería
I develop and maintain the company's internal management platform (private):
budgets in FIEBDC-3/BC3 format, certifications, invoicing, time tracking, per-project profitability,
client and partner portals, and PDF document generation.
*PHP · Symfony 7.4 · Doctrine · MySQL · Twig · PHPUnit · GitHub Actions*

## Tech stack

**AI and LLM engineering**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL_+_pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square)
![RAG](https://img.shields.io/badge/RAG_·_agents_·_evals-5A3FC0?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Bioinformatics and ML**
![Nextflow](https://img.shields.io/badge/Nextflow-0DC09D?style=flat-square&logo=nextflow&logoColor=white)
![nf-core](https://img.shields.io/badge/nf--core-24B064?style=flat-square)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat-square)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)

**Software engineering**
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)
![Symfony](https://img.shields.io/badge/Symfony-000000?style=flat-square&logo=symfony&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

## Get in touch

[LinkedIn](https://www.linkedin.com/in/pabloestepa) · pabloestepaalcaide011@gmail.com

I'm looking for remote roles in AI/LLM engineering. Happy to talk about RAG, agents, evals or AMR.
