---
layout: tutorial_hands_on

title: Optimization of ribosome A/P-site positioning in Ribo-seq data
zenodo_link: ''
questions:
- What is the meaning of offset in the Ribo-seq data analysis?
- Why do we need to correct this offset?

objectives:
- Learning how to correct the offset in the Ribo-seq data
time_estimation: '1h'
key_points:
- After we corrected the offset in Ribo-seq data, we could then predict ORFs accurately.
contributors:
- ldyang14

---


# Introduction
{:.no_toc}

<!-- This is a comment. -->

The step length is 3 nucleotides when ribosome sliding on the RNA. Therefore, there is an obvious triplet nucleotide periodicity for those data from Ribo-seq. We can not only infer the quality of Ribo-seq data but also determine the actively opening reading frames in the resolution of a single nucleotide. Furthermore, we could explain molecular mechanisms more precisely through the accurate location of actively translated regions. 

However, it leads to that a difficult problem was born in the analysis process for Ribo-seq data. Because there is an offset distance between 5'-end of ribosome-protected fragments and translating P-site. Nevertheless, we should calculate this offset precisely to deduce the really activated translated regions.

The reason why offset was produced is shown below. The first nucleotide of reads protected by ribosomes represents the margin by digesting of RNase. However, the real position for starting translating to a peptide is 16th nucleotide as shown in the figure below, which just represents the first nucleotide, not second or third, in the A-site. Thus we called that is in the frame, if 16th nucleotide of other reads of length 28nt is not located in the first position of A-site, we called that is not in the frame. Generally, most of reads are in the frame. Therefore, we should calculate and correct the offset of P/A-site prior to infer ORFs.

 ![Offset of Asite](../../images/optimization-of-PAsite/A-site.png "Offset of Asite cited from ({% cite liu2016prediction %})")

Therefore, lots of bioinformatics tools have been emerging to solve this problem. For example, the function `psite` in the [plastid](https://plastid.readthedocs.io/en/latest/index.html).

> ### Agenda
>
> In this tutorial, we will cover:
>
> 1. TOC
> {:toc}
>
{: .agenda}

# Calculate the offset

>### {% icon hands_on %} Hands-on: calculate the offset using plastid
>
>- {% icon tool %} plastid with following parameters:
>  - {% icon param-file %} *"annotation file"*: `gencode.v32.annotation.gtf` 
>  - {% icon param-select %} *"Landmark around which to build metagene profile"*: `cds_start` 
>  - {% icon param-text %} *"Nucleotides to include upstream of landmark"*: `50` 
>  - {% icon param-text %} *"Nucleotides to include downstream of landmark"*: `50` 
>  - ***TODO*** {% icon param-select %} *"alignment mapping functions"*: `Map read alignment to 5' position` 
>  - {% icon param-collection %} *""*: `aligned reads (BAM)` 
>
{: .hands_on}

We could get two outputs from psite, one of which graphically shows the distinct offset coupled with read length, and another is a table-separate format file that contains two columns,  one for read length and the other for the corresponding offset. This file could be used as input or a parameter to the subsequent 

analysis.



<img src="../../images/optimization-of-PAsite/RPF_WT_1_p_offsets.png" alt="Offset of P-site" title="Offset of P-site" style="zoom: 67%;" />

# Conclusion

{:.no_toc}

The P-site offset is the distance from the 5’ end of the read to the ribosomal P-site, in some methods, it can also be A-site. However, no matter what methods we used, the primary purpose is to detect and correct the offset for the prediction of ORFs accurately. 





