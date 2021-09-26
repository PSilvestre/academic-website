---
# Documentation: https://wowchemy.com/docs/managing-content/

title: 'Clonos: Consistent Causal Recovery for Highly-Available Streaming Dataflows'
subtitle: ''
summary: ''
authors:
- Pedro F. Silvestre
- Marios Fragkoulis
- Diomidis Spinellis
- Asterios Katsifodimos
tags:
- '"cloud computing"'
- '"stream processing"'
- '"exactly-once"'
- '"fault-tolerance"'
- '"high-availability"'
- '"consistency"'
categories: []
date: '2021-01-01'
lastmod: 2021-09-26T12:42:52+01:00
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
publishDate: '2021-09-26T11:42:52.580302Z'
publication_types:
- '1'
abstract: Stream processing lies in the backbone of modern businesses, being employed
  for mission critical applications such as real-time fraud detection, car-trip fare
  calculations, traffic management, and stock trading. Large-scale applications are
  executed by scale-out stream processing systems on thousands of long-lived operators,
  which are subject to failures. Recovering from failures fast and consistently are
  both top priorities, yet they are only partly satisfied by existing fault tolerance
  methods due to the strong assumptions these make. In particular, prior solutions
  fail to address consistency in the presence of nondeterminism, such as calls to
  external services, asynchronous timers and processing-time windows. This paper describes
  Clonos, a fault tolerance approach that achieves fast, local operator recovery with
  exactly-once guarantees and high availability by instantly switching to passive
  standby operators. Clonos enforces causally consistent recovery, including output
  deduplication, by tracking nondeterminism within the system through causal logging.
  To implement Clonos we re-engineered many of the internal subsystems of a state
  of the art stream processor. We evaluate Clonos' overhead and recovery on the Nexmark
  benchmark against Apache Flink. Clonos achieves instant recovery with negligible
  overhead and, unlike previous work, does not make assumptions on the deterministic
  nature of operators.
publication: '*Proceedings of the 2021 International Conference on Management of Data*'
url_pdf: https://doi.org/10.1145/3448016.3457320
doi: 10.1145/3448016.3457320
---
