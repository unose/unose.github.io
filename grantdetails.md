---
layout: default
title: Grant
permalink: /grantdetails/
---

<a href="javascript:history.back()" class="back-link">← back</a>


#### Intellectual Merit

My contributions centered on advancing **ML-driven software assurance techniques** to improve the **reliability, transparency, and maintainability of data-intensive scientific software**. The work addressed fundamental challenges in ML-based systems, including **debugging black-box models**, **validating data-driven behavior**, and **supporting developers in understanding evolving ML programs and large text corpora**.

Specifically, this project led to:

* **ML-based debugging and validation frameworks** for identifying data and model anomalies in ML programs.
* **Tool-supported software assurance techniques** that integrate program analysis, topic modeling, and human-in-the-loop visualization.
* **Scalable analysis of large bioengineering text corpora**, enabling systematic document retrieval, topic discovery, and knowledge exploration.
* **Deep learning–assisted code review and change inspection tools** that detect systematic and inconsistent changes in evolving software.

These contributions form a **coherent software engineering foundation for trustworthy ML systems**, directly supporting the center’s data-driven bioengineering mission while advancing generalizable SE research.

#### Broader Impacts

The project had strong workforce and educational impacts. I contributed to:

* **Workforce development and training**, including a hands-on research workshop involving **10 undergraduate and 13 graduate students**.
* Mentoring students at the intersection of **software engineering, machine learning, and data science**, preparing them for careers in **ML-enabled scientific software development**.
* Dissemination of **open research tools and IDE-based prototypes** that lower barriers for students and researchers to adopt ML-based software assurance techniques.

#### Publications Resulting from the Project

The SE and ML assurance thrust produced **peer-reviewed conference papers and journal article**, including work on:

* Topic modeling and visualization for bioengineering corpora
* Learning-to-rank for scientific document retrieval
* Topic mining for bug report analysis
* Deep learning–based code change inspection
* Debugging and validation of ML programs

This completed project provides a **strong foundation for extending ML-based techniques to secure and trustworthy software development**. The tools, methods, and insights developed for **software assurance in ML-driven scientific systems** directly inform future work on **secure software engineering, AI-assisted programming, and dependable ML-enabled infrastructure**.

---


<div class="pub-item">
  <div class="pub-title">
    Tool Support for Improving Software Quality in Machine Learning Programs (Information 2023)
  </div>
  <div class="pub-authors">
    Kwok Sun Cheng, Pei-Chi Huang, Tae-Hyuk Ahn, and Myoungkyu Song
  </div>
  <div class="pub-summary">
    This paper introduces <span class="highlight">MLVAL</span>, an interactive <span class="highlight">quality validation and debugging framework</span> designed to improve the <span class="highlight">software quality of machine learning (ML) programs</span>. MLVAL addresses challenges in validating <span class="highlight">data-driven and black-box ML systems</span> by enabling developers to inspect <span class="highlight">training data, learned features, and model evolution</span> through an <span class="highlight">Eclipse IDE plug-in</span>. The approach integrates <span class="highlight">human-in-the-loop visualization</span>, <span class="highlight">data version diffing</span>, and <span class="highlight">model behavior comparison</span> to diagnose <span class="highlight">ML-specific bugs and anomalies</span>. Evaluation on <span class="highlight">23,500 bioengineering documents</span> demonstrates improved <span class="highlight">model reliability, transparency, and maintainability</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
    Debugging Support for Machine Learning Applications in Bioengineering Text Corpora (COMPSAC 2022)
  </div>
  <div class="pub-authors">
    Kwok Sun Cheng, Tae-Hyuk Ahn, and Myoungkyu Song
  </div>
  <div class="pub-summary">
    This paper presents <span class="highlight">MLDBUG</span>, an interactive <span class="highlight">debugging framework for machine learning applications</span> that helps developers identify <span class="highlight">data and model anomalies</span> in <span class="highlight">black-box ML systems</span>. MLDBUG supports <span class="highlight">feature inspection</span>, <span class="highlight">data version diffing</span>, and <span class="highlight">model behavior comparison</span> through a <span class="highlight">human-in-the-loop visualization environment</span>. Implemented as an <span class="highlight">Eclipse IDE plug-in</span>, the approach enables effective <span class="highlight">model tuning and bug diagnosis</span>. Experiments on <span class="highlight">23,500 bioengineering documents</span> show that MLDBUG improves <span class="highlight">debugging efficiency</span> and enhances <span class="highlight">ML software reliability</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
    Learning to Rank Relevant Documents for Information Retrieval in Bioengineering Text Corpora (COMPSAC 2021)
  </div>
  <div class="pub-authors">
    Kwok Sun Cheng and Myoungkyu Song
  </div>
  <div class="pub-summary">
    This paper introduces <span class="highlight">LTREXPLORER</span>, a <span class="highlight">learning-to-rank–based information retrieval framework</span> for efficiently identifying <span class="highlight">relevant documents</span> in large-scale <span class="highlight">bioengineering text corpora</span>. The approach combines <span class="highlight">BM25</span>, <span class="highlight">vector space models</span>, and <span class="highlight">citation-aware features</span> extracted from document sections and reference networks. By leveraging <span class="highlight">29 domain-specific features</span>, LTREXPLORER achieves up to <span class="highlight">97% recall</span> and approximately <span class="highlight">85% ranking accuracy</span> on a corpus of <span class="highlight">23,500 documents</span>, significantly improving <span class="highlight">research productivity</span> and <span class="highlight">scalable literature exploration</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
    Analyzing Bug Reports by Topic Mining in Software Evolution (COMPSAC 2021)
  </div>
  <div class="pub-authors">
    Uy Nguyen, Kwok Sun Cheng, Samuel Sungmin Cho, and Myoungkyu Song
  </div>
  <div class="pub-summary">
    This paper presents <span class="highlight">BUGEXPLORER</span>, a <span class="highlight">topic mining–based framework</span> for analyzing <span class="highlight">bug reports</span> during <span class="highlight">software evolution</span>. Using <span class="highlight">LDA</span>, <span class="highlight">Hierarchical LDA</span>, and <span class="highlight">topical phrase mining</span>, the approach extracts <span class="highlight">latent semantic topics</span> from noisy bug report text. BUGEXPLORER supports <span class="highlight">bug triage</span>, <span class="highlight">similarity analysis</span>, and <span class="highlight">reviewer recommendation</span>. Evaluation on <span class="highlight">five large open-source projects</span> shows improved understanding of <span class="highlight">defect trends and topic evolution</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
    Tool Support for Code Change Inspection with Deep Learning in Evolving Software (EIT 2020)
  </div>
  <div class="pub-authors">
    Krishna Teja Ayinala, Kwok Sun Cheng, Kwangsung Oh, and Myoungkyu Song
  </div>
  <div class="pub-summary">
    This paper introduces <span class="highlight">SIL (Similar Changes Inspection with Deep Learning)</span>, a <span class="highlight">code review tool</span> that summarizes and inspects <span class="highlight">systematic and recurring code changes</span> in <span class="highlight">evolving software systems</span>. SIL combines <span class="highlight">AST-based edit scripts</span>, <span class="highlight">data and control dependence analysis</span>, and a <span class="highlight">deep learning classifier</span> trained on <span class="highlight">four clone types</span> mined from <span class="highlight">25,000 open-source programs</span>. Implemented as an <span class="highlight">Eclipse plug-in</span>, SIL detects <span class="highlight">inconsistent or missing changes</span>, reducing review effort and improving <span class="highlight">code review accuracy</span>.
  </div>
</div>

<div class="pub-item">
  <div class="pub-title">
    TopExplorer: Tool Support for Extracting and Visualizing Topic Models in Bioengineering Text Corpora (EIT 2020)
  </div>
  <div class="pub-authors">
    Kwok Sun Cheng, Zhipeng Wang, Pei-Chi Huang, Parvathi Chundi, and Myoungkyu Song
  </div>
  <div class="pub-summary">
    This paper presents <span class="highlight">TopExplorer</span>, an <span class="highlight">interactive topic modeling and visualization tool</span> for exploring <span class="highlight">large-scale bioengineering document collections</span>. TopExplorer integrates <span class="highlight">LDA</span>, <span class="highlight">Hierarchical LDA</span>, and <span class="highlight">phrase mining</span> to uncover <span class="highlight">latent thematic structures</span> and relationships across documents. The tool provides <span class="highlight">interactive visual analytics</span>, including topic distributions, hierarchical topic trees, and document-level views. Evaluation on <span class="highlight">600 bioengineering articles</span> shows improved <span class="highlight">knowledge discovery</span>, <span class="highlight">trend analysis</span>, and <span class="highlight">decision-making</span>.
  </div>
</div>
