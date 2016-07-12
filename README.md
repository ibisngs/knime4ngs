# KNIME4NGS Test Workflows

Two test workflows show how to connect the nodes of the KNIME4NGS toolkit to create powerful analysis pipelines for variant calling (DNA-seq) and differential expression analysis (RNA-seq).
Small sample datasets are provided for both workflows which allow you to execute all nodes locally within a short period of time.

The following descriptions of the workflows assume that you have downloaded KNIME and installed the KNIME4NGS extension as described in the [manual](https://github.com/ibisngs/knime4ngs/raw/gh-pages/knime4ngs_manual.pdf).
Further, you have to download and unzip the provided [resource bundle](https://github.com/ibisngs/knime4ngs/archive/resource.zip).
We recommend to feed the KNIME4NGS preference page with the resource bundle reference genome and variant sets before importing the test workflows as it facilitates their configuration a lot.
Then, the provided workflows can easily be imported into KNIME via *Import KNIME Workflow...* in the *File* menu.

## Variant Calling

The [variant calling workflow](https://github.com/ibisngs/knime4ngs/raw/master/KNIME4NGS_Test_VarCalling.zip) covers all steps from raw read quality assessment to variant annotation.

![](figures/VarCalling.png)

Before executing the workflow, you have open the node dialog of the FileLoader and select NA12877\_R1.fastq and NA12877\_R2.fastq in the folder VarCalling of the resource bundle as first and second fastQ input file.
Then, the status lights of all nodes should change to yellow which means that you can execute the complete workflow now.

## Differential Expression

The [differential expression workflow](https://github.com/ibisngs/knime4ngs/raw/master/KNIME4NGS_Test_DiffExpression.zip) first creates a genome index used by the STAR aligner.
Then, it iterates over RNA-seq data of 8 individuals, merges the read counts and uses DESeq to perform differential expression analysis.

![](figures/DiffExpression.png)

The upper FileLoader of the workflow has to be loaded with the fastA file of the reference gnome (chr16.fa in the reference genome folder of the provided resources).
The lower FileLoader takes a list of fastQ files as input (diff\_exp\_fastq.list in the DiffExpression folder of the resources).
Then, set the path to the annotation file in the FeatureCounts node dialog which corresponds to the path to the file Homo_sapiens.GRCh37.75.chr16.gtf in your resources folder.
Finally, you have to add the path to the sample_cond.tsv in the CSVReader node.
Although, the status lights of some nodes are still red you can now execute the workflow.




