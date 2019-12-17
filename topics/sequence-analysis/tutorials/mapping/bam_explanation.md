A BAM ([Binary Alignment Map](https://en.wikipedia.org/wiki/SAM_(file_format))) file is a compressed, binary file storing the sequences mapped to a reference sequence. 

> ### {% icon hands_on %} Hands-on: Inspect a BAM/SAM file
>
> 1. Inspect the {% icon param-file %} output of **{{ include.mapper }}** {% icon tool %}
>
{: .hands_on}

<<<<<<< HEAD
A BAM file (or a SAM file, the non compressed version) consists of:

- A header section (the lines starting with `@`) containing metadata, in particular the chromosome names and lengths (lines starting with the `@SQ` symbol)
=======
A BAM file (or a SAM file, the non-compressed version) consists of:

- A header section (the lines starting with `@`) containing metadata particularly the chromosome names and lengths (lines starting with the `@SQ` symbol)
>>>>>>> 4c20cc70897846b93043c2fed195d7efcffac751
- An alignment section consisting of a table with 11 mandatory fields, as well as a variable number of optional fields:

    Col | Field | Type | Brief Description
    --- | --- | --- | ---
    1 | QNAME | String | Query template NAME
<<<<<<< HEAD
    2 | FLAG | Integer | bitwise FLAG
=======
    2 | FLAG | Integer | Bitwise FLAG
>>>>>>> 4c20cc70897846b93043c2fed195d7efcffac751
    3 | RNAME | String | References sequence NAME
    4 | POS | Integer | 1- based leftmost mapping POSition
    5 | MAPQ | Integer | MAPping Quality
    6 | CIGAR | String | CIGAR String
    7 | RNEXT | String | Ref. name of the mate/next read
    8 | PNEXT | Integer | Position of the mate/next read
<<<<<<< HEAD
    9 | TLEN | Integer | observed Template LENgth
    10 | SEQ | String | segment SEQuence
=======
    9 | TLEN | Integer | Observed Template LENgth
    10 | SEQ | String | Segment SEQuence
>>>>>>> 4c20cc70897846b93043c2fed195d7efcffac751
    11 | QUAL | String | ASCII of Phred-scaled base QUALity+33 

> ### {% icon question %} Questions
>
> 1. Which information do you find in a SAM/BAM file?
> 2. What is the additional information compared to a FASTQ file?
>
> > ### {% icon solution %} Solution
> > 1. Sequences and quality information, like a FASTQ
> > 2. Mapping information, Location of the read on the chromosome, Mapping quality, etc
> {: .solution }
{: .question}
