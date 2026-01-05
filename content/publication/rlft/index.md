---
# Documentation: https://wowchemy.com/docs/managing-content/

title: 'Systems Opportunities for LLM Fine-Tuning using Reinforcement Learning'
subtitle: ''
summary: ''
authors:
- Pedro F. Silvestre
- Peter Pietzuch
tags:
- '"Deep Learning"'
- '"LLMs"'
- '"Large Language Models"'
- '"Reinforcement Learning"'
- '"RLFT"'
- '"Fine-Tuning"'
- '"RLVR"'
- '"RLHF"'
categories: []
date: '2026-01-01'
lastmod: 2026-01-01T12:42:52+01:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ''
  focal_point: ''
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
publishDate: '2025-03-30T11:42:52.580302Z'
publication_types:
- '1'
abstract: 
    Reinforcement learning-based fine-tuning (RLFT) has emerged as a crucial workload for enhancing large language models (LLMs). RLFT workflows are challenging, involving nested loops, multiple models, dynamically shaped tensors and interleaving sequential generation and parallel inference tasks. Despite these complexities, current RLFT engines rely on coarse-grained algorithm representations, treating each component as an independently optimized black-box. As a result, RLFT engines suffer from redundant computations, scheduling overhead, inefficient memory management, and missed opportunities for parallelism.
    We argue that a fine-grained representation is needed to enable holistic optimization for RLFT workloads. Additionally, we demonstrate that existing declarative deep learning engines fail to optimize RLFT workloads end-to-end due to their need for static tensor shapes and loop bounds, leading to excessive peak memory usage and unnecessary computations. Through micro-benchmarks, we quantify these inefficiencies and show that addressing them could enable more efficient and flexible execution. We propose an RLFT system design based on a fine-granularity representation, opening the door to generalizable optimizations, and paving the way for more scalable and efficient RLFT systems.
publication: '*Proceedings of the 5th Workshop on Machine Learning and Systems*'
url_pdf: https://dl.acm.org/doi/pdf/10.1145/3721146.3721944
doi: 10.1145/3721146.3721944
---
