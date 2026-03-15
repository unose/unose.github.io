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

## 2025 ICSE Towards Understanding the Characteristics of Code Generation Errors Made by Large Language Models

**High-Level Summary**

The paper provides a deep empirical analysis of the types of coding mistakes LLMs produce. The authors focus on bridging the gap in understanding why and how LLMs fail at code generation, which is crucial for developing better automated repair and localization techniques.

**Summary**

Wang et al. present an empirical study of code generation failures in LLMs by analyzing 557 incorrect Python solutions produced by six models on 164 HumanEval tasks, with the goal of moving beyond pass-rate evaluation toward a deeper understanding of how LLM-generated code fails. The paper develops a fine-grained taxonomy of errors along two complementary dimensions—semantic root causes and syntactic error locations—resulting in 13 semantic characteristics in 7 categories and 14 syntactic characteristics in 7 categories, derived through open coding and thematic analysis with strong inter-rater agreement. Their results show that LLM failures are typically non-trivial, multi-line, and often semantically complex rather than simple syntax mistakes; across models, the most common semantic problems are wrong logical direction and incorrect condition, while the most common syntactic problems are missing or incorrect code blocks. The study further shows that these incorrect solutions are usually far from the correct programs, implying substantial repair effort, and that longer prompts and more complex target solutions are strongly associated with failure, with roughly 60% of outputs becoming garbage code when prompts exceed 150 words or correct solutions exceed 12 lines of code. Compared with prior work that focused mainly on compilation errors, crashes, or code translation bugs, this paper contributes a broader cross-model analysis of NL-to-code failures and argues that fine-grained error characteristics can support better fault localization, repair, and correctness estimation for LLM-generated code.  

**Possible Direction**

If we utilize this paper's idea, ...

**Methodology HighlightsStudy Subjects:** 

- Evaluated LLMs: CodeGen-16B, InCoder-1.3B, GPT-3.5, GPT-4, SantaCoder, and StarCoder.

- Dataset: They used the HumanEval benchmark, which contains 164 Python programming tasks.
  
- Analysis Approach: The researchers manually investigated 557 incorrect code solutions. They invested approximately 328 person-hours into open coding and thematic analysis to build a detailed error taxonomy.
  
- Taxonomy Dimensions: Errors were categorized by semantic characteristics (the high-level root causes, like a wrong logical direction) and syntactic characteristics (the specific error locations, like an incorrect code block).

**Key Findings Complexity of Errors:** 

- LLMs rarely make simple, single-line syntax errors; instead, they generate non-trivial, multi-line errors that require substantial effort to repair.

- Common Pitfalls: Across all evaluated models, the most frequent semantic errors were a "wrong (logical) direction" and an "incorrect condition". Syntactically, over 40% of errors involved missing or incorrect entire code blocks.

- Task Complexity Boundaries: The models struggle significantly as task complexity increases. When a prompt exceeded 150 words or the correct solution required more than 12 lines of code, about 60% of the LLM outputs were classified as "Garbage Code" (meaningless or irrelevant code).

- Partial vs. Complete Failures: Code that failed all test cases often contained meaningless code snippets, whereas code that passed some test cases usually suffered from missing steps or subtle if-condition errors.

- Repair Difficulty: The incorrect code generated by LLMs deviates significantly from the ground-truth solutions, demonstrated by high Levenshtein distances and low CodeBERT scores.

**Strategic Gaps & Brainstorming Angles**

The authors note several limitations that map perfectly to emerging challenges in software engineering and security. Here are a few immediate gaps we could exploit: 

- Beyond Function-Level Python: This study is strictly limited to standalone, function-level Python tasks from HumanEval.

  - Idea: How do these error characteristics shift when generating code in complex, repository-level environments with rich dependencies? We could investigate error generation in enterprise-scale codebases, particularly focusing on how LLMs handle software supply chain integrations or API usages.

- Security and Vulnerability Generation: The taxonomy focuses on logical correctness and test pass rates.

  - Idea: We could pivot this methodology to focus purely on the security characteristics of LLM errors. When an LLM misunderstands a prompt, what classes of vulnerabilities (e.g., injection flaws, improper authentication) does it hallucinate into existence?

- Automating the Taxonomy for Large-Scale Analysis: The authors spent 328 person-hours labeling 557 snippets.

  - Idea: We could develop a specialized LLM-based framework (perhaps using chain-of-thought or multi-agent debate) to automatically classify code generation errors at scale. This could lead to a real-time, automated "reviewer" that catches and categorizes LLM errors before a human developer even sees them.

---

__Treating code authorship as a binary "Human vs. LLM" is an outdated paradigm that peer reviewers will instantly tear apart. In modern workflows, code is co-authored. It exists on a spectrum.__

* Using AST (Abstract Syntax Tree) delta/diff analysis to track atomic changes is a methodological rigor required for a top-tier SE venue like ICSE, FSE, or MSR. It completely invalidates the anchor paper's reliance on simple Levenshtein distances (which only measure text edits, not structural or logical changes).

* Define "Mixed Authorship" and a methodology around AST tracking.

### 1. Defining the "Spectrum of Authorship"

Instead of a binary classification, we can define a metric—let's call it the **LLM Node Survival Rate (LNSR)** or the **Authorship Index**.

* **100% LLM:** The raw, initial generation. Every AST node was generated by the AI.
* **Mixed (e.g., 70% LLM / 30% Human):** The human developer kept the overarching structure (class definitions, loops) but modified specific nodes (e.g., updated variable names, inserted a missing `if` condition, or deleted a hallucinated method call).
* **0% LLM (Total Rewrite):** The human developer deleted the LLM's entire generated subtree and replaced it with their own AST nodes.

### 2. The AST Delta Analysis Pipeline

To measure the exact "fix effort" evolution across a Pull Request, we evaluate the atomic changes between the `Before` version (the raw LLM commit) and the `After` versions (the human's subsequent commits). Since tracking these atomic changes at scale is complex, we could build our analysis pipeline around a robust Python AST parser to extract the exact node-level deltas between the raw LLM output and the human-merged PR.

We would categorize the human's "fix effort" into four standard AST edit actions:

* **Update (Value Changes):** The human changed the value of a node. For example, the LLM generated `len(x) > 0` and the human updated it to `len(x) >= 0`. This represents *low-effort logic tweaking*.
* **Insert (Missing Context):** The human had to add new nodes. For example, adding an exception-handling `try/except` block around the LLM's code. This maps directly to the anchor paper's "Missing multiple steps" semantic error and represents *medium-to-high effort*.
* **Delete (Hallucination Removal):** The human had to prune nodes. For example, deleting a call to a hallucinated API or removing an unnecessary loop. This represents *debugging effort*.
* **Move (Structural Refactoring):** The human kept the LLM's code but moved the AST nodes to a different part of the tree (e.g., pulling a variable declaration outside of a loop). This represents *architectural effort*.

### 3. Why This Elevates the Research

By tracking atomic AST changes, we can empirically answer questions that text-based diffs cannot:

1. **Where do humans spend the most effort?** Do humans spend more time inserting missing logic (Insert), fixing hallucinated parameters (Update), or deleting irrelevant code clones (Delete)?
2. **The "Deceptive Error" Threshold:** We might find that PRs with the smallest text-based edit distance (e.g., just updating a single boolean node from `True` to `False`) actually take the longest time in the PR review cycle to merge, proving that subtle LLM logical errors require massive cognitive effort to detect and fix.

### 4. Setting the Baseline

To execute this, we still need that "Node Zero"—the untouched LLM generation. We could pull data from PRs opened by autonomous coding agents (where the first commit is provably 100% LLM) and then track the human reviewers' subsequent AST-level changes.
