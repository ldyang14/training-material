---
layout: tutorial_hands_on

title: Normalization of Ribo-Seq reads
zenodo_link: ''
questions:
- Which biological questions are addressed by the tutorial?
- Which bioinformatics techniques are important to know for this type of data?
objectives:
- The learning objectives are the goals of the tutorial
- They will be informed by your audience and will communicate to them and to yourself
  what you should focus on during the course
- They are single sentences describing what a learner should be able to do once they
  have completed the tutorial
- You can use Bloom's Taxonomy to write effective learning objectives
time_estimation: ''
key_points:
- The take-home messages
- They will appear at the end of the tutorial
contributors:
- ldyang14

---


# Introduction
{:.no_toc}

<!-- This is a comment. -->

After mapping was completed, we would obtain detailedly mapped results, which usually is SAM or BAM format.  Spontaneously, we would wonder the expression of interested genes to compare, explore, and analyze differences for a customized experiment condition. Hence, how should we carry out this process? Firstly, we should extract information of read counts from BAM/SAM file using tools like `featureCounts`. Is that it? Of course not. Since library depth and gene lengths are different in each sample, we need to normalize read counts mapped on each gene for comparisons between them (an example is shown below). It is important to execute this step because we would analyze accurately only after that read counts were normalized exactly.

![Normalization of reads]( https://izabelcavassim.files.wordpress.com/2015/03/screenshot-from-2015-03-08-2245511.png "[Normalization of reads](https://izabelcavassim.files.wordpress.com/2015/03/screenshot-from-2015-03-08-2245511.png)")

> ### Agenda
>
> In this tutorial, we will cover:
>
> 1. TOC
> {:toc}
>
{: .agenda}









> ### {% icon hands_on %} Questions
>
> 
> 
>{: .hands_on}



# Conclusion
{:.no_toc}

