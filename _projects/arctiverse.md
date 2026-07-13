---
title: "Genome Assembly and Annotation"
date: 2025-07-01
category: "Research"
context: "Internship M2 — IBPS"
technologies: ["Python", "Snakemake", "Docker"]
links:
    - text: "Assembly Pipeline Github"
      url: "https://github.com/MaiDeme/genomeAssemble"
    - text: "Annotation Pipeline Github"
      url: "https://github.com/MaiDeme/genomeAnnotation"
layout: project
description: "I developed pipelines for the assembly and annotation of algal genomes using short reads and long Nanopore reads."
permalink: /projects/arctiverse/
---
I worked on developing two pipelines for the assembly and annotation of algal genomes. The first pipeline focused on assembling high-quality genomes from Nanopore long-read using tools like Flye or Masurca. The second pipeline was dedicated to annotating these genomes, utilizing existing framework like Funannotate and BRAKER and integrating RNA-seq data for improved gene prediction.

Here is an overview of the assembly pipeline:
<figure>
  <img src="/assets/images/assembly.png" alt="Genome Assembly Pipeline" style=" 
  max-width:600px; width:100%; height:auto; display:block; margin:auto; border-radius:5px;">
</figure>

And here is an overview of the annotation pipeline:
<figure>
  <img src="/assets/images/annotation.png" alt="Genome Annotation Pipeline" style=" 
  max-width:600px; width:100%; height:auto; display:block; margin:auto; border-radius:5px;">
</figure>