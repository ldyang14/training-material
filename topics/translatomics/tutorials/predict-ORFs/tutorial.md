---
layout: tutorial_hands_on

title: Detection of actively translated ORFs using Ribo-Seq data
zenodo_link: ''
questions:
- How many kinds of open reading frames (ORFs) are in the cell?
- Why is it useful for us to understand regulatory mechanisms of gene by predicting ORFs? 
objectives:
- To know the various categories of ORFs
- Learning how to predict ORFs through translatomics data
time_estimation: '1H'
key_points:
- Complex and sophisticated biological process might be reasoned from the alternative translated peptides.
contributors:
- ldyang14

---


# Introduction
{:.no_toc}

<!-- This is a comment. -->

Predicting ORFs activated translation accurately is the foundation for us to explore and understand the physiological process deeply. Fortunately, ribosome profiling provides us a convenient and reliable tool to study gene information at the translational level.

Currently, annotations of the coding sequence (CDS) is conservative, because the annotation is usually inferred from homologous sequences of protein databases and EST databases. However, translation, the most critical step in the delivery of gene information, is neglected by the conventional annotation of the CDS. The translation is the direct participant for decoding information in the gene sequences, thus leading to them become the proteins with a specific function. Moreover, conventional annotation of the CDS does not indicate optional coding regions like upstream ORFs (uORF), which were proved to have regulated the expression of downstream CDS in the previous study. Hence, substantial genome information is waiting for us to discover.



![Categories of ORFs](../../images/predict-ORFs/category-of-ORFs.png "Categories of ORFs (cited from {% cite ji2015many %})")

As we all know, ribosomes are an important spot to execute the process of the translation and reads from ribosome profiling are RNA fragments enclosed by ribosomes. Therefore, ribosome profiling provides us insight into detailed and complicated information delivered by the translation. We can predict ORFs through mapping reads against the genome or transcriptome. These ORFs not only come from annotated CDSs, but also isoforms of CDS, novel, and so on. Previous studies have shown that some sequences only activate translation but not produce peptides to play regulatory functions. Therefore, it is meaningful for us to predict these ORFs to understand the physiological process. For example, some ORFs will translate cancer-specific antigen, thus we can predict these ORFs to design drugs specifically targeted cancer cells. 



![Categories of ORFs](../../images/predict-ORFs/Category-of-ORFs-2.png "Categories of ORFs (cited from {% cite ji2015many %})")




> ### Agenda
>
> In this tutorial, we will cover:
>
> 1. TOC
> {:toc}
>
{: .agenda}

***TODO***

# Conclusion

{:.no_toc}

Diversity ORFs lead to more complex and diverse biological functions and processes, hence, we can understand the mechanisms of gene regulation more deeply throgh predicting and decucing the expression of ORFs in a gene.