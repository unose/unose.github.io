# Potential Research Directions: Code Smells and Pull Request Dynamics

**Context:**
This memo outlines potential research avenues building upon the findings of the 2023 exploratory study, *"Code smells in pull requests: An exploratory study"* (Azeem et al., SPE), and surrounding literature on software design decay in pull-based development.

---

## 1. Granular, Smell-Specific Prediction Models

The baseline study grouped pull requests (PRs) into a binary **"smelly"** or **"non-smelly"** classification if any of four target smells were detected:

* God Class
* Data Class
* Long Method
* Long Parameter List

### Research Gap

Not all code smells share the same origin or predictive metadata. For instance:

* A **Large Class** might strongly correlate with code churn.
* **Naming Inconsistencies** may correlate with contributor inexperience.

### Proposed Direction

Train distinct machine learning classifiers to predict **which specific type of smell** is likely present based on PR metadata.

This directly addresses future work identified by the authors and enables:

* Targeted automated triage pipelines
* Reviewer assignment based on expertise
* More precise technical debt tracking

---

## 2. AI-Assisted Detection for Subjective and Semantic Smells

The baseline study relied on **PMD**, a traditional static analysis tool, to establish ground truth. The authors noted a threat to internal validity because rule-based tools may not perfectly capture all smell types.

### Research Gap

Traditional static analysis struggles with subjective or semantic design flaws such as:

* Cognitive Complexity
* Spaghetti Code
* Poor Logging

These require understanding of intent and semantics.

### Proposed Direction

Evaluate the effectiveness of modern **Large Language Models (LLMs)** as automated reviewers to detect subjective design flaws in PR diffs.

This study would:

* Compare precision and recall of LLMs vs. traditional tools (e.g., PMD)
* Evaluate false positive rates
* Assess reliability of generative AI in semantic smell detection

---

## 3. The Collaborative Impact of Specific Design Flaws

The study established that PRs containing code smells:

* Are more complex
* Have longer latency times
* Require more discussion
* Generate more review comments

### Research Gap

Because smells were grouped together, it remains unclear:

> Which specific design flaws cause the most friction in collaborative workflows?

### Proposed Direction

Conduct a mixed-methods analysis of PR comment threads to determine:

* Which smells trigger the most reviewer pushback
* Which structural issues stall CI/CD pipelines
* Whether structural smells (e.g., Feature Envy) create more delay than localized smells (e.g., Long Method)

---

## 4. Intersecting Test Smells with Refactoring-Inducing PRs

The 2023 SPE paper focused on application-level design flaws. However, broader literature (e.g., Soares et al., 2020) highlights the prevalence of **Test Smells**.

### Research Gap

The relationship between a decaying test suite and PR integration friction remains underexplored in pull-based development.

### Proposed Direction

Investigate correlations between:

* PRs introducing **Test Smells**
* The likelihood of future **refactoring-inducing PRs**

This research would analyze whether a smelly test suite:

* Increases integration hesitation
* Slows CI/CD workflows
* Amplifies long-term technical debt

---

# Research Papers on Code Smells and Pull Requests

### 2023 — SPE

**Code Smells in Pull Requests: An Exploratory Study**
Muhammad Anwer, Saad Shafiq, Atif Mashkoor
[https://onlinelibrary.wiley.com/doi/pdfdirect/10.1002/spe.3283](https://onlinelibrary.wiley.com/doi/pdfdirect/10.1002/spe.3283)

---

### 2023 — ESEM

**Beyond the Code: Investigating the Effects of Pull Request Conversations on Design Decay**
Osmar Barbosa, Aline Valente, Daniel Coutinho, Francisco Farias
[https://scholar.google.com/scholar?q=Beyond+the+Code:+Investigating+the+Effects+of+Pull+Request+Conversations+on+Design+Decay](https://scholar.google.com/scholar?q=Beyond+the+Code:+Investigating+the+Effects+of+Pull+Request+Conversations+on+Design+Decay)

---

### 2023 — ICSME

**How Do Developers Improve Code Readability? An Empirical Study of Pull Requests**
Carlos E. C. Dantas, Anderson M. Rocha, Marcelo A. Maia
[https://scholar.google.com/scholar?q=How+Do+Developers+Improve+Code+Readability?+An+Empirical+Study+of+Pull+Requests](https://scholar.google.com/scholar?q=How+Do+Developers+Improve+Code+Readability?+An+Empirical+Study+of+Pull+Requests)

---

### 2021 — ESEM

**An Empirical Study on Refactoring-Inducing Pull Requests**
Filipe Castro, Nikolaos Tsantalis, Tom Mens
[https://scholar.google.com/scholar?q=An+Empirical+Study+on+Refactoring-Inducing+Pull+Requests](https://scholar.google.com/scholar?q=An+Empirical+Study+on+Refactoring-Inducing+Pull+Requests)

---

### 2021 — JSS

**Does Code Quality Affect Pull Request Acceptance? An Empirical Study**
Valentina Lenarduzzi, Veli Nikkola, Nyyti Saarimäki, Davide Taibi
[https://doi.org/10.1016/j.jss.2020.110806](https://doi.org/10.1016/j.jss.2020.110806)

---

### 2020 — SANER

**On the Effect of Code Review on Code Smells**
Luca Pascarella, Davide Spadini, Fabio Palomba, Magiel Bruntink, Alberto Bacchelli
[https://arxiv.org/pdf/1912.10098](https://arxiv.org/pdf/1912.10098)

---

### 2019 — ESE

**How Does Code Style Inconsistency Affect Pull Request Integration? An Exploratory Study on 117 GitHub Projects**
Weiqin Zou, Jifeng Xuan, Xiaoyuan Xie, Zhenyu Chen, Baowen Xu
[https://link.springer.com/article/10.1007/s10664-019-09720-x](https://link.springer.com/article/10.1007/s10664-019-09720-x)

---
