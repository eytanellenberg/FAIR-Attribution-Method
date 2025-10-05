

# FAIR-Attribution-Method

**Author:** Eytan Ellenberg, MD, MPH, PhD
**Affiliation:** Research Office, Medical Affairs, National Insurance Institute of Israel, Jerusalem
**Contact:** [eytane@nioi.gov.il](mailto:eytane@nioi.gov.il)
**License:** Open-access (for academic and educational use)
**Associated publication:** *From Population Evidence to Individual Attribution: The FAIR Framework for Causal Assessment in Occupational Medicine* (submitted to *Occupational Medicine*, OUP, 2025)

---

## 🧠 Overview

The **FAIR Framework** (*Filtering evidence, Association quantification, Individual partitioning, Reasoned interpretation*) provides a structured, transparent approach for **quantitative causal attribution** in occupational and environmental medicine.

FAIR integrates systematic evidence appraisal, quantitative risk estimation, and **Shapley-based partitioning** of multifactorial risks to translate epidemiological data into legally interpretable, individual-level causal shares.

This repository hosts the computational proof-of-concept accompanying the manuscript.

---

## ⚙️ Contents

* `/scripts/` – R and Python functions for FAIR computation

  * `fair_shapley.R`: main allocation algorithm
  * `association_module.R`: RR/OR conversion and baseline incidence integration
  * `sensitivity_analysis.R`: Monte Carlo and additive vs. multiplicative checks
* `/data/` – example datasets and meta-analytic parameters
* `/docs/` – supplementary materials, OHAT appraisal examples, and workflow diagrams
* `/results/` – example FAIR outputs (Shapley shares, sensitivity tables, figures)

---

## 🚀 How to Use

### 1️⃣ Install dependencies

In R:

```r
install.packages(c("tidyverse", "data.table", "dplyr", "reshape2"))
```

### 2️⃣ Run example computation

```r
source("scripts/fair_shapley.R")
example <- fair_compute("data/example_mesothelioma.csv")
print(example)
```

### 3️⃣ Reproduce figures

```r
source("scripts/plot_shapley.R")
plot_fair_results(example)
```

Outputs include:

* Individual causal shares (%)
* Attributable risks per 100,000
* Comparison with AF/PAF and Bayesian probability of causation

---

## 🧩 FAIR Principles

This repository adheres to **FAIR data principles**:

* **Findable** – structured metadata and clear indexing
* **Accessible** – open-source repository
* **Interoperable** – standard CSV/JSON data and R scripts
* **Reusable** – transparent documentation and modular code

---

## 🔬 Citation

If you use or adapt the FAIR methodology, please cite as:

> Ellenberg E. *From Population Evidence to Individual Attribution: The FAIR Framework for Causal Assessment in Occupational Medicine.* Submitted to *Occupational Medicine (Oxford University Press)*, 2025.

---

## 🧭 Future Development (FAIR 2.0)

The next version will integrate:

* **Causal Shapley Values (CSV)** for dependence structures
* **Monte Carlo simulation** for uncertainty quantification
* **Bayesian inference** for probabilistic attribution
* **Interactive dashboards** for occupational physicians and legal experts

---

## ⚠️ Disclaimer

FAIR is designed for research and methodological purposes.
It is **not a diagnostic or adjudicative tool** and should always be interpreted by qualified experts within medico-legal and ethical frameworks.

---

Souhaites-tu que je te prépare la **version ultra-compacte (≈160 caractères)** à mettre dans la courte *description* du dépôt (sous le titre GitHub) ?
