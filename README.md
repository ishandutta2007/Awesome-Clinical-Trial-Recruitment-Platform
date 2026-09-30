# Awesome-Clinical-Trial-Recruitment-Platform

## Top Clinical Trial Recruitment Platforms Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Patient Matching, Automated Prescreening, Site Feasibility & Recruitment Automation*

**Last updated: September 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Clinical Trial Recruitment**. These tools help sponsors, CROs, and research sites identify eligible patients, automate prescreening against trial criteria, and accelerate enrollment.



**Examples** include Antidote, Deep 6 AI, Trialbee, AutoCruitment, Clara Health, SubjectWell, TriNetX, Inato, Lightship, Power, Curebase, PatientWing, Bio-Optronics, TrialScope, StudyKIK, Clariness, Reify Health, and TrialSpark (the category leaders).



**Open-source emphasis**: Clinical trial recruitment has a **mature and production-proven open-source ecosystem**. **recruIT** is a cloud-native system deployed across 5 German university hospitals with a SUS usability score of 79.9/100 . **CancerTrialMatch** is an open-source biomarker-based matching application published in *Bioinformatics* . **MatchMiner** (Dana-Farber) is a computational platform for genomic-based trial matching . **LLM-Match** achieves superior performance over proprietary GPT-4-based tools using only open-source models . This section documents these production-grade solutions.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents



- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Antidote](https://antidote.me/)**  

  Patient-facing clinical trial matching platform. Connects patients with trials via search and AI-powered matching.



- **[Deep 6 AI](https://deep6.ai/)**  

  AI-powered clinical trial matching platform. Acquired by Tempus in 2023, combining genomic testing with EHR-based matching.



- **[Trialbee](https://trialbee.com/)**  

  Patient recruitment and matching platform connecting patients with trials across therapeutic areas.



- **[AutoCruitment](https://autocruitment.com/)**  

  Patient recruitment platform using digital marketing and prescreening to accelerate trial enrollment.



- **[SubjectWell](https://subjectwell.com/)**  

  Patient recruitment marketplace connecting patients with trial opportunities.



- **[TriNetX](https://www.trinetx.com/)**  

  Global health research network providing real-world data and clinical trial matching.



- **[Inato](https://www.inato.com/)**  

  Clinical trial site and patient matching platform connecting sponsors with community sites.



- **[Reify Health (StudyTeam)](https://reifyhealth.com/)**  

  Clinical trial recruitment and retention platform. StudyTeam modernizes sponsor-site collaboration for enrollment.



- **[Curebase](https://www.curebase.com/)**  

  Decentralized clinical trial platform with patient matching and recruitment capabilities.



- **[TrialSpark](https://www.trialspark.com/)**  

  Technology-enabled trial execution platform with patient recruitment and decentralized capabilities.



## Open-Source GitHub Projects



### Production-Deployed Recruitment Systems



- **[recruIT](https://gitlab.ukdd.de/pub/num-sn/recruit)**  

  **The most mature open-source clinical trial recruitment support system.** **Deployed across 5 German university hospitals** as part of the NUM Study Network and MIRACUM consortium . **Architecture**: Based on **OMOP CDM** for patient data and **HL7 FHIR** for interoperability. Uses **OHDSI Atlas** to define trial eligibility criteria as cohort definitions. Three modules: **Query Module** (queries OMOP via OHDSI WebAPI), **List Module** (screening list UI with patient ID, birth year, last known location), **Notification Module** (email alerts for new candidates) . **Usability**: SUS score **79.9/100** from 19 end-users across 5 hospitals . Container-based deployment with Kubernetes support. **Open source**.



- **[CancerTrialMatch](https://github.com/AveraSD/CancerTrialMatch)**  

  **Open-source biomarker-based trial matching application published in *Bioinformatics* (2025).** Developed at Avera Cancer Institute. **Key capability**: Captures structured clinical trial data and matches patients based on **disease characteristics and sequencing profiles** . Uses **OncoTree classification** for disease types and captures biomarker details (mutations, copy numbers, fusions). Retrieves trial data via **ClinicalTrials.gov API** with manual entry for biomarkers. Built with **R Shiny, MongoDB, and Docker**. Semi-automated interface. Deployed on Windows 11/WSL2 with Docker Compose . **Open source**.



- **[MatchMiner](https://github.com/matchminer/matchminer)**  

  **Open-source computational platform for matching patient-specific genomic profiles to precision cancer medicine clinical trials.** Developed at Dana-Farber Cancer Institute . Originally rules-based, now incorporates **AI to analyze unstructured EHR data** (clinical notes) to extract prior treatments, disease stage, and other trial-relevant features. Supports **all patients** at an institution. Already in use at **Princess Margaret Cancer Centre**. Has supported **400+ patient enrollments** at Dana-Farber, with patients matched through MatchMiner enrolling **22% faster** than traditional methods . **Open source**.



### AI/LLM-Powered Matching Models



- **[LLM-Match](https://github.com/bioIKEA/LLMMatch)**  

  **Open-source patient matching model based on LLMs and Retrieval-Augmented Generation (RAG).** Published in 2025 . **Key innovation**: Exclusively leverages **open-source models**, proving they can achieve **superior performance** over proprietary GPT-4-based tools when properly fine-tuned . Combines RAG with fine-tuning and a classification head. Evaluated on multiple benchmark datasets (n2c2, SIGIR24, TREC 2021, TREC 2022). Provides a scalable, transparent alternative to black-box AI . **Open source**.



- **[TrialGPT](https://github.com/ncbi-nlp/TrialGPT)**  

  **LLM framework for patient-trial matching by evaluating clinical trial eligibility criteria against patient notes** . Uses GPT-4 to assess patient eligibility. Foundation for subsequent open-source matching frameworks. **Open source**.



- **[AI Clinical Trial Matching (sacredvoid)](https://github.com/sacredvoid/ai_clinical_trial)**  

  **Full open-source pipeline for matching patients to trials using vector embeddings and LLMs.** **Architecture**: Patient data from CSV → SQLite database; clinical trials scraped from clinicaltrials.gov → ChromaDB vector database; patient profiles and trial criteria embedded using **SentenceTransformer (all-MiniLM-L6-v2)**; 3-stage matching algorithm (vector similarity search → expert LLM assessment → result generation) . Uses **Llama 3.2 3B-Instruct** via Hugging Face/OpenRouter. **Python-based** . **Open source**.



### Trial Curation & Feasibility



- **[Databricks Site Feasibility Workbench](https://github.com/databricks-industry-solutions/site-feasibility-workbench-open)**  

  **Open-source clinical trial site feasibility and patient access platform.** Provides **AI/BI Genie Space** for natural language feasibility queries, **LightGBM enrollment velocity predictions**, **SHAP feature attributions** (top 5 drivers per study×site), and **RWE patient access estimates** . Deploys as a **Databricks App** with Unity Catalog, SQL Warehouse, and optional Lakebase (PostgreSQL). **All data is fully synthetic** — designed as a template for real deployments . **Open source**.



- **[Blue-button (open-source)](https://ascopubs.org/doi/10.1200/JCO.2025.43.16_suppl.TPS1658)**  

  **Open-source clinical trial matching tool developed in collaboration with ACS CAN and MITRE Corporation** . **SMART-on-FHIR tool** that automatically extracts deidentified patient data (cancer type, stage, biomarkers) from EHR systems and queries external matching services via **FHIR mCODE standard** . Uses **FHIR ResearchStudy resource format** for trial matches. Currently in prospective randomized trial at UTSW and Tampa General Hospital. **Open source**.



### Additional Strong Open-Source Options



- **Production-Deployed**: **recruIT** (5 German hospitals, SUS 79.9) , **CancerTrialMatch** (Avera, *Bioinformatics*) , **MatchMiner** (Dana-Farber, 400+ enrollments) .

- **AI/LLM Models**: **LLM-Match** (open-source models outperform GPT-4) , **TrialGPT** (GPT-4-based eligibility) , **AI Clinical Trial Matching** (vector embeddings + Llama) .

- **Feasibility & Curation**: **Databricks Site Feasibility Workbench** (LightGBM + SHAP) , **Blue-button** (SMART-on-FHIR, FHIR mCODE) .

- **HL7 FHIR Integration**: **recruIT** (OMOP + FHIR), **Blue-button** (SMART-on-FHIR) .



**Frameworks for building custom systems**: Combine **recruIT** for population-level prescreening with OMOP/FHIR, **CancerTrialMatch** or **MatchMiner** for biomarker/genomic-based matching, **LLM-Match** or **TrialGPT** for LLM-powered eligibility assessment, and **Blue-button** for EHR-integrated regional matching via FHIR mCODE. Add **PostgreSQL/OMOP CDM** for patient data and **Docker** for deployment.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Clinical trial recruitment platforms handle sensitive patient health data; ensure compliance with HIPAA, GDPR, 21 CFR Part 11, and applicable research regulations.

- **Open-source reality**: The open-source ecosystem for clinical trial recruitment is **mature and production-proven**. **recruIT** is deployed across 5 German university hospitals with strong usability scores . **CancerTrialMatch** and **MatchMiner** are published, production-deployed systems at major cancer centers . **LLM-Match** demonstrates that open-source models can outperform proprietary alternatives . **Blue-button** is in prospective randomized trials at academic and community hospitals . For **enterprise-scale multi-therapeutic recruitment** with global site networks and dedicated patient support, commercial platforms (Antidote, Trialbee, SubjectWell, Reify Health) remain the primary choice — but open-source alternatives are **genuinely viable for institutions with technical capacity**.



---



**Made for clinical research coordinators, trial recruitment specialists, informatics teams, and site administrators.**

Let's make clinical trial recruitment more open, transparent, and patient-centered.
