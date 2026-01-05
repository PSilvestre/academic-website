---
title: On a Shared Composable Toolchain for Dataflow Systems
subtitle: a.k.a. Thinking about an LLVM for Systems

# Summary for listings and search engines
summary: An outline for the design of a shared (LLVM-like) toolchain but for dataflow systems

# Link this post with a project
projects: []

# Date published
date: "2023-12-05T00:00:00Z"

lastmod: "2023-12-05T00:00:00Z"

draft: true

featured: true

image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/-t5YUoHW6zRo)'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- Dataflow Systems
- Systems
- Architecture
- LLVM
- Fault Tolerance

categories:
- Technical Notes


bibFile: content/post/llvm-for-dataflow/bib.json 
---

{{< toc >}}

%An intro that sets out the project and my goals with this post

%Apache and Unix foundation projects sort-of offer a solution: seperate distributed systems that fulfil different roles and can be composed mostly through
RPC. However, this is not precisely what I'm thinking

## The Shared Structure of Dataflow Systems

## The Unique Structure of Certain Systems

## What would this look like
%A figure of the layers

### Program parsing

### Algebras as the IR

### Optimizer/Transformation Pipeline

### Efficient MPS dataplane

### Fault-Tolerance

### Storage

## Cited Bibliography
{{< bibliography cited >}} 
