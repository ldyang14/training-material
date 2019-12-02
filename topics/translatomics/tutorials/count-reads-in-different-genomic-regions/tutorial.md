---

layout: tutorial_hands_on

title: Counting Ribo-Seq reads in different genomic regions
zenodo_link: ''
questions:
- How is the distribution of reads on the different genomic features?
objectives:
- Learning the method to measure read counts on genomic regions
time_estimation: '0.5h'
key_points:
- We could know more details about gene regulation at the translational level through investigating the distribution of reads on the genomic features.
contributors:
- ldyang14
- IceApink
---


# Introduction
{:.no_toc}

<!-- This is a comment. -->

Distinct from RNA-seq data, reads from Ribo-Seq data usually located in the translated genomic regions. However, reads resided in the UTR or intronic regions are also worthy of attention due to their underlying regulatory functions. Supposing that there is a gene we interested in, we wonder to know whether expression of 5'UTR makes an effect on it, thus we first need to observe the distribution of reads on that gene. For example, it is likely that the expression of 5'UTR on the gene displayed in the figure below inhibited the expression of CDS. However, this phenomenon is not observed within the RNA-seq data. Hence, the distribution of reads on the genomic features provides new insight into the regulatory mechanism of gene expression.



![Distribution of reads on the genome](../../images/count-reads-in-different-genomic-regions/reads_on_genome.png "Distribution of reads on the genome (cited from {% cite kallehauge2017ribosome %})")

> ### Agenda
>
> In this tutorial, we will cover:
>
> 1. TOC
> {:toc}
>
{: .agenda}


# Distribution of reads on the genomic features

## Using RiboProfiling

> ### {% icon hands_on %} Hands-on: Count reads on genomic features with RiboProfiling
>
> - Run **RiboProfiling** {% icon tool %} with the following parameters
>   - {% icon param-collection %}*"BAM File to analysis"*: `aligned reads (BAM)`
>  - ***TO DO*** {% icon param-select %}*"Select genome"*: `hg38`
>    
>
> {: .hands_on}

A lot of results were produced by `RiboProfiling`, but we only focused on the result of read counts on different genomic regions. As shown below, most of reads distributed on the CDS as we expected.

<img src="../../images/count-reads-in-different-genomic-regions/reads_in_genomic_regions.png" alt="Distribution of reads in different genomic regions" title="Distribution of reads in different genomic regions" style="zoom: 80%;" />

## Using Ribo-SeqC

***TODO*** We can also get this result using `Ribo-SeqC` as described in the [Quality of Ribo-Seq data](). This results is displayed below. 

![Distribution of reads on the genomic features](../../images/count-reads-in-different-genomic-regions/riboseqc1_counts_in_features.png "Distribution of reads on the different genomic features")

# Conclusion

{:.no_toc}

It is helpful to us for understanding the regulatory of gene expression through investigating the reads on the different genomic features. In the past, we can not explore the heterogeneity of gene expression on different gene features limited by technology, but now ribosome profiling offers an opportunity for us to discover and explore the heterogeneous expression of genes. Hence, we could reveal more details of gene expression and understand molecular mechanisms more deeply.









