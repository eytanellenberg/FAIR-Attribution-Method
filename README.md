# FAIR-Attribution-Method v1.1

**Author:** Eytan Ellenberg MD MPH PhD  
**Affiliation:** Research Office, Medical Affairs, National Insurance Institute of Israel  
**License:** CC BY 4.0  
**Release Date:** October 2025  

---

## 📘 Overview

This repository contains the full implementation of the **FAIR framework**  
(*Filtering evidence, Association quantification, Individual partitioning, Reasoned interpretation*).  
FAIR provides a structured and transparent methodology for **individual causal attribution** in occupational medicine.

Version 1.1 corresponds to the manuscript submitted to  
**_Occupational Medicine (Oxford University Press)_**, October 2025.

FAIR 1.1 includes:
- Deterministic Shapley allocation of excess risk (standard FAIR)
- **Monte Carlo FAIR** module for stochastic uncertainty propagation
- Conceptual **causal Shapley extension** (Heskes 2020)
- Fully auditable, open-source R workflow compliant with FAIR data principles

---

## 🔬 Methodological background

| Step | Purpose | Core methods |
|------|----------|--------------|
| **F – Filtering evidence** | Systematic selection and bias appraisal (OHAT) | Exclusion of high-risk meta-analyses |
| **A – Association quantification** | Extraction of adjusted RR/OR and baseline risk (p₀) | Conversion OR → RR (Zhang & Yu 1998) |
| **I – Individual partitioning** | Shapley value allocation of excess risk | Game-theoretic fairness (efficiency, symmetry, additivity) |
| **R – Reasoned interpretation** | Expert contextualization and iterative refinement | Clinical, anatomical, and latency plausibility checks |

Future extensions (FAIR–SQS) combine **causal Shapley [Heskes 2020]** with **Monte Carlo** simulation to model correlated exposures.

---
# FAIR-Attribution-Method v1.1

**Author:** Eytan Ellenberg MD MPH PhD  
**Affiliation:** Research Office, Medical Affairs, National Insurance Institute of Israel  
**License:** CC BY 4.0  
**Release Date:** October 2025  

---

## 📘 Overview

This repository contains the full implementation of the **FAIR framework**  
(*Filtering evidence, Association quantification, Individual partitioning, Reasoned interpretation*).  
FAIR provides a structured and transparent methodology for **individual causal attribution** in occupational medicine.

Version 1.1 corresponds to the manuscript submitted to  
**_Occupational Medicine (Oxford University Press)_**, October 2025.

FAIR 1.1 includes:
- Deterministic Shapley allocation of excess risk (standard FAIR)
- **Monte Carlo FAIR** module for stochastic uncertainty propagation
- Conceptual **causal Shapley extension** (Heskes 2020)
- Fully auditable, open-source R workflow compliant with FAIR data principles

---

## 🔬 Methodological background

| Step | Purpose | Core methods |
|------|----------|--------------|
| **F – Filtering evidence** | Systematic selection and bias appraisal (OHAT) | Exclusion of high-risk meta-analyses |
| **A – Association quantification** | Extraction of adjusted RR/OR and baseline risk (p₀) | Conversion OR → RR (Zhang & Yu 1998) |
| **I – Individual partitioning** | Shapley value allocation of excess risk | Game-theoretic fairness (efficiency, symmetry, additivity) |
| **R – Reasoned interpretation** | Expert contextualization and iterative refinement | Clinical, anatomical, and latency plausibility checks |

Future extensions (FAIR–SQS) combine **causal Shapley [Heskes 2020]** with **Monte Carlo** simulation to model correlated exposures.

---

## 📂 Repository structure


---

## ⚙️ Installation

```r
# Install dependencies
install.packages(c("tidyverse", "gtools"))

# Clone repository
git clone https://github.com/eytanellenberg/FAIR-Attribution-Method.git
setwd("FAIR-Attribution-Method")

# Load core functions
source("FAIR_core.R")
source("FAIR_functions.R")
RR_list <- c(asbestos = 6.7, smoking = 1.2)
p0 <- 1.8e-5
result <- shapley_allocation(RR_list, p0)
print(result)
simulate_FAI(RR_mean = 1.8, RR_low = 1.4, RR_high = 2.2,
             p0_mean = 0.0008, p0_low = 0.0006, p0_high = 0.001)
Output interpretation

RAI (Individual Attributable Risk): estimated share of disease risk due to exposure.

Shapley share: proportion of total excess risk attributed fairly among exposures.

FAI ↔ R cycle: iterative re-computation after new information or expert reassessment.

🧮 Validation & transparency

All data = public meta-analytic or registry sources

OHAT scoring sheets → Annex 1

Code and Monte Carlo outputs → Annex 2

Reproducibility tested on 10 000 simulations / case

📚 Citation

Ellenberg E. The FAIR Framework: Structured Reasoning for Individual Causal Attribution in Occupational Medicine.
Submitted to Occupational Medicine (OUP), 2025.
FAIR-Attribution-Method v1.1 [Computer software]. GitHub. DOI: to be assigned via Zenodo.

🔗 Data availability & DOI

All materials follow the FAIR data principles (Findable, Accessible, Interoperable, Reusable).
A Zenodo DOI will be minted automatically upon publication of this release.

🧩 Acknowledgments

This repository accompanies the FAIR framework development within the
National Insurance Institute of Israel (Medical Affairs Office).
Statistical support: anonymous reviewers of Monte Carlo methods.

🧠 License

Creative Commons Attribution 4.0 International (CC BY 4.0)
You are free to reuse, modify, and redistribute with proper attribution.

Contact: eytane@nioi.gov.il

GitHub: https://github.com/eytanellenberg/FAIR-Attribution-Method

## 📂 Repository structure

