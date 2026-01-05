---
# Documentation: https://wowchemy.com/docs/managing-content/

title: 'Tempo: Compiled Dynamic Deep Learning with Symbolic Dependence Graphs'
subtitle: ''
summary: ''
authors:
- Pedro F. Silvestre
- Peter Pietzuch
tags:
- '"Deep Learning"'
- '"Reinforcement Learning"'
- '"Deep Learning Systems"'
- '"Reinforcement Learning Systems"'
- '"Computational Graphs"'
- '"Symbolic Computational Graphs"'
- '"Temporal Dimensions"'
- '"Polyhedral Scheduling"'
- '"Memory Management"'
- '"Compilation"'
- '"Optimization"'
- '"Linear Algebra"'
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
publishDate: '2025-10-13T11:42:52.580302Z'
publication_types:
- '1'
abstract: >-
    Deep learning (DL) algorithms are often defined in terms of temporal relationships: a tensor at one timestep may depend on tensors from earlier or later timesteps. Such dynamic dependencies (and corresponding dynamic tensor shapes) are difficult to express and optimize: while eager DL systems support such dynamism, they cannot apply compiler-based optimizations; graph-based systems require static tensor shapes, which forces users to pad tensors or break-up programs into multiple static graphs.
    We describe Tempo, a new DL system that combines the dynamism of eager execution with the whole-program optimizations of graph-based compilation. Tempo achieves this through a declarative programming model with recurrent tensors, which include explicit temporal dimensions. Temporal dimensions can be indexed using symbolic expressions to express dynamic dependencies on past and future tensors. Based on this, Tempo constructs a symbolic dependence graph, which concisely encodes dynamic dependencies between operators, and applies whole-program optimizations, such as algebraic simplifications, vectorization, tiling, and fusion. By tiling dynamic dependencies into static-size blocks, Tempo can also reuse existing static code-generators. It then uses a polyhedral model to find a feasible execution schedule, which includes memory management operations. We show that Tempo achieves a 7× speedup over JAX for Llama-3.2-3B decoding; for reinforcement learning algorithms, Tempo achieves a 54× speedup, with 16× lower peak memory usage.
publication: '*Proceedings of the ACM SIGOPS 31st Symposium on Operating Systems Principles*'
url_pdf: https://dl.acm.org/doi/pdf/10.1145/3731569.3764840
doi: 10.1145/3731569.3764840
---
