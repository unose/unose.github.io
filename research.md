---
layout: default
title: Research
permalink: /research/
---

# Research

## Research Overview

My research focuses on **software engineering** and **program analysis**, with the goal of improving the **reliability**, **maintainability**, and **developer productivity** of real-world software systems.  
I am particularly interested in combining **automated analysis** with **learning-based techniques**, including **large language models (LLMs)**, to support developers across the software lifecycle.

---

## Research Areas

### Program Analysis and Software Evolution

-   Analysis of **software changes**, **refactorings**, and **recurring modification patterns**
-   Techniques to support **code review**, **regression testing**, and **program comprehension**
-   Improving the **transparency** and **interpretability** of software evolution

### Software Correctness

-   Automated detection and explanation of **software defects**
-   Integration of **static analysis**, **statistical methods**, and **machine learning**
-   Developer-facing tools that provide **actionable feedback**

### AI & LLM-assisted Software Engineering

-   Combining **large language models (LLMs)** with **traditional program analysis**
-   Applications to **code completion**, **code summarization**, and **human–AI collaboration**
-   Emphasis on **reliability** and **trustworthiness** in developer tools

### AI-assisted Programming Education

-   Intelligent tutoring systems for programming education
-   Automated feedback to support **effective software development practices**
-   Reinforcing **fundamental software engineering principles**

---

## Selected Recent Publications and Projects

<div class="pub-item">
<div class="pub-title">
Intelligent Code Completion by a Unified Multi-task Learning with a Large Language Model (SERA 2025)
</div>
<div class="pub-authors">
Shradha Maharjan, Meng Xia, Tae-Hyuk Ahn, Myoungkyu Song
</div>
<div class="pub-summary">
This work introduces CODECOM, a deep learning-based code completion technique that integrates a large language model with program analysis to provide more accurate and context-aware code suggestions. By leveraging source code tokens, abstract syntax trees, and program dependencies, CODECOM significantly outperforms existing approaches and helps developers write correct code more efficiently.
</div>
<div class="pub-summary">
This work introduces CODECOM, a <span class="highlight">deep learning-based code completion</span> technique that integrates a <span class="highlight">large language model</span> with <span class="highlight">program analysis</span> to provide more accurate and <span class="highlight">context-aware code suggestions</span>. By leveraging <span class="highlight">source code tokens</span>, <span class="highlight">abstract syntax trees</span>, and <span class="highlight">program dependencies</span>, CODECOM significantly outperforms existing approaches and helps developers write correct code more efficiently.
</div>
</div>

<div class="pub-item">
<div class="pub-title">
Automated Code Summarization by Training Large Language Models with Crowdsourced Knowledge (SERA 2025)
</div>
<div class="pub-authors">
Meng Xia, Shradha Maharjan, and Myoungkyu Song
</div>
<div class="pub-summary">
This paper presents DEEPKNOWLEDGE, an <span class="highlight">automated code summarization</span> approach that leverages a <span class="highlight">large language model</span> trained with <span class="highlight">crowdsourced knowledge</span> from GitHub and Stack Overflow. By integrating real-world coding examples and developer discussions, the approach generates more accurate and <span class="highlight">context-aware summaries</span> that explain code behavior, implementation rationale, and usage guidelines. Extensive evaluation on <span class="highlight">large-scale Java datasets</span> shows that DEEPKNOWLEDGE significantly outperforms state-of-the-art techniques, improving <span class="highlight">BLEU scores</span> by up to 39%, and demonstrating its effectiveness in supporting <span class="highlight">program comprehension</span> and maintaining up-to-date documentation in evolving software systems.
</div>
</div>

<div class="pub-item">
  <div class="pub-title">
  SYNC: Synergistic Annotation Collaboration between Humans and LLMs for Enhanced Model Training (SERA 2025)
  </div>
  <div class="pub-authors">
  Tommy Le, Will Taylor, Shradha Maharjan, Meng Xia, and Myoungkyu Song
  </div>
  <div class="pub-summary">
  This paper introduces SYNC, a <span class="highlight">human-LLM collaborative annotation framework</span> designed to improve the accuracy and reliability of <span class="highlight">data annotation</span> for Stack Overflow datasets. SYNC combines multiple <span class="highlight">automated annotation strategies</span>—including TF-IDF-based lexical matching, <span class="highlight">transformer-based semantic similarity</span>, and <span class="highlight">code-aware embeddings</span> using UniXcoder—with human verification and refinement. By integrating automated efficiency with human oversight through web, mobile, and desktop interfaces, the approach produces higher-quality annotations that better support downstream tasks such as <span class="highlight">code retrieval</span>, summarization, and analysis in <span class="highlight">large language model-based programming assistants</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
  SYNCode: Synergistic Human-LLM Collaboration for Enhanced Data Annotation (Information 2025, extended version of SERA 2025)
  </div>
  <div class="pub-authors">
  Meng Xia, Shradha Maharjan, Tommy Le, Will Taylor, Myoungkyu Song
  </div>
  <div class="pub-summary">
  This paper presents SYNCode, a <span class="highlight">human-LLM collaborative framework</span> for high-quality data annotation in <span class="highlight">code-centric domains</span> such as Stack Overflow. The approach combines <span class="highlight">lexical and semantic analysis</span> with <span class="highlight">code-aware representations</span> to generate initial annotations, which are then iteratively validated and refined by human annotators through an <span class="highlight">interactive system</span>. Experimental results show that SYNCode improves annotation accuracy and scalability while reducing bias, supporting downstream software engineering and <span class="highlight">language model-based analysis tasks</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
  A Machine-Learning Approach to API Usage Learning for Detecting API Misuse Errors
  </div>
  <div class="pub-authors">
  PIs: Myoungkyu Song (UNO), Harvey Siy (UNO), Youngjin Kwon (UNMC), Kwangsung Oh (UNO), and Na Zhong (UNO)
  </div>
  <div class="pub-summary">
  Nebraska Research Initiative (NRI), University of Nebraska System. Project Period: 2023-2025.<br>
  This Nebraska Research Initiative-funded project investigates <span class="highlight">learning-based approaches</span> for <span class="highlight">modeling correct API usage</span> and <span class="highlight">detecting API misuse errors</span>. By combining <span class="highlight">program analysis</span> with <span class="highlight">machine learning</span> and <span class="highlight">large language models</span>, the project supports research on <span class="highlight">code completion</span>, <span class="highlight">code summarization</span>, and developer-facing program understanding tools, contributing to multiple recent peer-reviewed publications.
  </div>
</div>

<!-- 
---

## Research Grants and Projects

### A Machine-Learning Approach to API Usage Learning for Detecting API Misuse Errors

**Funding Agency:** Nebraska Research Initiative (NRI), University of Nebraska System  
**Project Period:** 2023–2025  
**PIs:** Myoungkyu Song (UNO), Harvey Siy (UNO), Yeongjin Gwon (UNMC), Kwangsung Oh (UNO), Xin Zhong (UNO)

This project investigates learning-based approaches for modeling correct API usage and detecting API misuse errors by combining program analysis with machine learning. The outcomes support research on code completion, code summarization, and developer-facing program understanding tools, contributing to multiple peer-reviewed publications. -->

---

## Collaboration

I actively collaborate with faculty and students across software engineering,
AI/ML, programming languages, automated program analysis, and large language models.
I am also committed to extending these efforts beyond academia and actively seek
partnerships with industry leaders and national laboratories to translate research
innovations into practical solutions and validate research outcomes in real-world
software ecosystems.
