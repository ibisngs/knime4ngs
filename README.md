**DiffExpression** 
The folder contains all files required by the KNIME4NGS\_Test\_DiffExpression workflow.
The data used in this workflow was generated by a RNA-seq experiment which aimed to identify transcriptomic changes in four primary human airwary smooth muscle cells treated with dexamethasone.
For more description of the experiment see the [PubMed entry 24926665](http://www.ncbi.nlm.nih.gov/pubmed/24926665) and for raw data see the [GEO entry GSE52778](http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE52778).
- SRR*.fastq.gz: RNA-seq read pairs of 8 individuals.
- diff_exp_fastq.list: List of all paired FastQ files. Serves as input for the FileLoader node.
- sample_cond.tsv: Assignment of each of the 8 samples to the treated (dex) or untreated (untrt) group.
- Homo_sapiens.GRCh37.75.chr16.gtf.gz: Annotation file needed for the FeatureCounts node.

**Exome_VarCal**

**RefGenome**

**VariantSets**

