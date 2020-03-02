2/27/20

This command creates the index files to be used in mapping

*Input*

`bwa index RCG16s.fa`

*Output*

```shell
```

---------------------------------------------------------------------
This creates various index files in current directory: 
RCG16s.fa       RCG16s.fa.ann   RCG16s.fa.pacRCG16s.fa.amb   RCG16s.fa.bwt   RCG16s.fa.sa

---------------------------------------------------------------------

This command runs the bwa aligner of the trimmed 148 sample reads on to RCG16s.fa

*Input*

`bwa mem RCG16s.fa /Users/blakemcmurray/Desktop/Workspaces/BhayaScripts/alignmentStuff/Hotspr2Sample148_2/12651.1.273621.AGGAACCT-AGGTTCCT.filter-METAGENOME.fastq.gz > RCG16s_sam148.sam`

*Output*

```shell
NA
```

---------------------------------------------------------------------
The resulting sam file took up much too much space on my disk and as a result did not complete.  I will add other flags and 
attempt to output a compressed file to save space

---------------------------------------------------------------------
This command runs bwa mem with a flag -A 500 to speed up run time.  

*Input*

`bwa mem -A 500 RCG16s.fa /Users/blakemcmurray/Desktop/Workspaces/BhayaScripts/alignmentStuff/Hotspr2Sample148_2/12651.1.273621.AGGAACCT-AGGTTCCT.filter-METAGENOME.fastq.gz | gzip -3 > RCG16s_sam148.sam.gz`

*Output*

```shell
```

---------------------------------------------------------------------
**Still need to understand what the -A 500 does to the alignment

output: RCG16s_sam148.sam.gz

Now I will use samtools to learn about the alignment.

---------------------------------------------------------------------

This command converts the sam file into a bam file

*Input*

`samtools view -S -b RCG16s_sam148.sam.gz > RCG16s_sam148.bam`

*Output*

```shell
NA
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command outputs relevant info about the alignment

*Input*

`samtools flagstat RCG16s_sam148.bam`

*Output*

```shell
440487992 + 0 in total (QC-passed reads + QC-failed reads)
0 + 0 secondary
0 + 0 supplementary
0 + 0 duplicates
115625 + 0 mapped (0.03% : N/A)
0 + 0 paired in sequencing
0 + 0 read1
0 + 0 read2
0 + 0 properly paired (N/A : N/A)
0 + 0 with itself and mate mapped
0 + 0 singletons (N/A : N/A)
0 + 0 with mate mapped to a different chr
0 + 0 with mate mapped to a different chr (mapQ>=5)
```

---------------------------------------------------------------------
115625 mapped reads for rosei flexus (around 0.03 % of the reads).
Let's look at the quality of those reads.  Find statistics on those reads.

---------------------------------------------------------------------

This command runs bwa mem on osa (same command for osb)

*Input*

`bwa mem -A 500 OSA.fa /Users/blakemcmurray/Desktop/Workspaces/BhayaScripts/alignmentStuff/Hotspr2Sample148_2/12651.1.273621.AGGAACCT-AGGTTCCT.filter-METAGENOME.fastq.gz | samtools view -S -b > OSA16s_samp148.bam`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command creates more thorough statistics regarding the alignment using samtools stats.  Same command for other alignments.

*Input*

`samtools stats OSA16s_samp148.bam > OSA16s_samp148_stats.txt`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command pulls all the mapped reads from the initial file into a separate file

*Input*

`samtools view -b -F 4 RCG16s_sam148.bam > RCG16s_samp148_mapped.bam`

*Output*

```shell
```

---------------------------------------------------------------------
The same was done for the other files.  Now we can analyze which reads mapped, the scores, and attempt to bin the mappings to a single reference.  

---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------
This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

This command

*Input*

`x`

*Output*

```shell
```

---------------------------------------------------------------------
---------------------------------------------------------------------

