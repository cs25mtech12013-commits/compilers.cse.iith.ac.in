---
title: "Research Domains"
layout: textlay
excerpt: "IITH Compilers Team -- Research"
sitemap: false
permalink: /research/
---
<style>
.dp-img {
     margin-bottom: 0px; 
     margin-top: 0px; 
     border-radius: 0%; 
}

.dp {
	outline: 0;
        cursor: pointer
}
.iterate
{
        display: flex;
        flex-direction: row;
}
</style>



## Research Domains
Our broad research is in Programming Languages and Compilers. More specifically, following are the research areas we are currently working on.

### Static analysis and Program Optimizations
* Compile time program analysis is indispensable for both program optimization as well as program verification.
* Detecting bugs at compile time reduces the risk of runtime failures, which can be fatal for safety critical systems. 
* Program optimization can reduce the execution time of the program, thereby enhancing the performance and increasing user experience.
<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=SA+Opt] %}
</div>


----

### Machine Learning for Compilers
A well defined sequence of compiler optimizations will have a strong impact on performance of the program. Optimization decisions for achieving optimal performance are complex and are computationally hard. Hence machine learning techniques can help in making making better optimization decisions.



<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects  --query @*[domain=ML4Compilers]%}
</div>


----

### Compilers for Deep Learning
With the emergence of various deep learning models and hardware architectures, it is infeasible to write optimized code for every architecture. There are various techniques to optimize the code but the search space is huge. Hence deep learning techniques helps to design good heuristics to select optimized code.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=Compilers4ML] %}
</div>


----

### Polyhedral Compilation
A class of programs called affine programs can be represented as integer polyhedra to perform high level transformations such as loop-fusion, loop-distribution, tiling, skewing, loop-rotaion, etc. to optimize for runtime. Polyhedral compilation can perform complex transformations to generate architecture dependent optimized code.



<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects  --query @*[domain=Polyhedral] %}
</div>


----

### Code Compilance and Security
Safety of critical systems is of utmost importance as the failure or malfunction of one can lead to significant increase in the safety risk for the people or environment involved. Code Compliance checkers are hence designed to verify the various coding standards developed to ensure the safety of critical systems namely MISRA, CERT, ISO26262. 
<details>
<summary class="dp" markdown='span'> <b>CCCheckers</b> </summary>

##### A code compliance checker that can verify programs according to the MISRA standards for C. 
</details>
----

### Compiler Optimizations for Heterogeneous Systems
Heterogeneous systems combining CPUs, GPUs, and FPGAs offer immense performance potential but pose a trade-off between ease of programming and optimization. While abstractions like Unified Memory simplify development, they often degrade performance, whereas streams and asynchronous APIs improve efficiency but increase complexity. To address this, we propose compiler optimizations that enable cooperative CPU-GPU execution. Our compiler framework, GSOHC, introduces hetero-sync motion optimization to improve CPU utilization by relocating global barriers, while our frameworks UVMemcpy and StreamAlloc provide efficient yet user-friendly memory management. Together, these solutions enhance both programmability and performance in heterogeneous systems.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=HeteroSys] %}
</div>

----

### Machine Learning for Programming Languages
While traditional program analysis tools are very powerful, they become challenging to use in real settings due to their whole-program requirements and scalability issues. As AI systems learn from examples, they overcome some of these challenges easily; however, current Code Language Models (CLMs) such as CodeBERT, GraphCodeBERT, UniXcoder, and Codex still struggle to capture the deeper program semantics required for building advanced developer productivity tools. At IITH, we are developing lightweight CLMs that can accurately perform tasks such as vulnerability detection, bug classification, and code summarization. By combining targeted input representations, pattern-aware encodings, and efficient classifiers, our models capture deep semantic information and overcome token length constraints, making advanced code intelligence more practical and sustainable. As part of this project, we collaborate with Microsoft Research, IIT Kharagpur, and Deakin University.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=ML4PL] %}
</div>

----

### Parallelization
The goal of this project is to address the problem of many applications not taking full advantage of the parallelism provided by massively parallel GPUs due to limitations in: efficiently utilizing GPU memory, understanding and leveraging domain-specific data patterns, etc. We provide efficient parallel algorithms and application-level optimizations for achieving high performance on GPUs. At IITH, we are currently working on two sub-problems: (1) Efficient Approximate Nearest Neighbour search on high-dimensional billion-point data (coming from deep learning-based embeddings) using a single GPU, (2) Multi-Query optimization for subgraph isomorphism search on GPUs. Along the same lines, in the past, we worked on developing an efficient tensor transposition library (TTLG) for GPUs.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=Parallelization] %}
</div>

----

### Concurrency Testing
Testing the correctness of a concurrent system is challenging. We have worked on two problems which deal with automated testing of concurrent systems: (1) A Language-agnostic Concurrency Testing Library: Designed for developers to build their own custom systematic testing solutions. The library detects concurrency bugs by taking over the scheduling of concurrent operations (tasks/threads/actors etc.) and systematically exploring the various interleavings of operations. (2) Testing Storage-backed Applications Against Weak Isolation Levels: Develops a mock storage system that exercises weak behaviors possible under multiple isolation levels to detect assertion violations in a database/KV-store application. The operational semantics of this storage system is based on axiomatic definitions of various weak isolation levels.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=ConcurrencyTesting] %}
</div>

----

### Program Analysis for Code Refactoring
This research involves proposing efficient static analyses (mainly points-to analyses) for automatic identification of challenging refactoring opportunities in object-oriented software, with particular emphasis on the issues that occur when the refactoring tools are coupled into resource-bound environments like IDEs (Integrated Development Environments).

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=CodeRefactoring] %}
</div>

----

### Superoptimization for Verified Systems
Traditional compiler optimizations are often ineffective for verified systems such as eBPF due to strict verifier constraints. Stochastic superoptimization helps discover efficient equivalent programs through search-based transformations. Our work improves this process using semantic-guided analysis and verifier-aware pruning to eliminate invalid candidates early and improve optimization efficiency.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=Superoptimization] %}
</div>

----

### Data Migration Validation using NeuroSymbolic AI and LLMs
Traditional data migration tools rely on strict, deterministic rules that fail when dealing with messy enterprise data involving subjective interpretations or vague business logic. Large Language Models (LLMs) can automatically formalize these ambiguous rules, but their outputs are prone to hallucinations and are often impossible to verify using standard mathematical solvers (like SMT). Our work introduces a pre-verification engine that uses static analysis to catch these unverifiable rules early, combining property-based testing and human-in-the-loop feedback to guarantee both semantic accuracy and data integrity.

<style>
  .bib ol{
    list-style: none;
    display: flex;
    padding-left : 0;
  }
  .bib li{
    margin-bottom: 1.5em;
  }
  </style>
<div class="bib">
{% bibliography --template bibtemplate_projects --query @*[domain=DataMigration] %}
</div>

----

<br/>

