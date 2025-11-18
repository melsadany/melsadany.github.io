---
layout: default
title: Single-Cell Multi-Omics of Brain Stimulation
---

# Single-Cell Multi-Omics of Human Brain Stimulation

## Overview
Engineered an end-to-end computational pipeline for single-nuclei multi-omics (RNA+ATAC) data from an in vivo human brain electrical stimulation study.

## Key Results

### Cell Type Identification
![UMAP of Cell Types](assets/images/brain_stim_umap.png)
*UMAP visualization of major brain cell types identified through reference-based annotation*

### Differential Expression
![Volcano Plot](assets/images/brain_stim_volcano.png)
*Volcano plot showing significantly differentially expressed genes in excitatory neurons following stimulation*

### Cross-Species Validation
![RRHO Analysis](assets/images/brain_stim_rrho.png)
*Rank-Rank Hypergeometric Overlap analysis showing conserved transcriptional changes between human and mouse models*

## Methods
- **Single-nuclei multi-omics** processing with Cell Ranger ARC
- **Cell type annotation** using Allen Institute reference
- **Differential expression** with mixed-effects models (lmmSeq)
- **Cross-species comparison** using RRHO analysis

## Technologies
R, Seurat, RRHO2, lmmSeq, Python, HPC

[Back to Portfolio](../index.md)
