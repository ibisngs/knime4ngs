# KNIME4NGS Test Workflows

Two test workflows show how to connect the nodes of the KNIME4NGS toolkit to create powerful analysis pipelines for variant calling (DNA-seq) and differential expression analysis (RNA-seq).
Small sample datasets are provided for both workflows which allow you to execute all nodes locally within a short period of time.

The following descriptions of the workflows assume that you have downloaded KNIME and installed the KNIME4NGS extension as described in the [manual](https://github.com/ibisngs/knime4ngs/raw/gh-pages/knime4ngs_manual.pdf).

We recommend to feed the KNIME4NGS preference page with the respective execution binaries before importing the test workflows as it minimizes repetitive node configuration. Most of the binaries are provided and can easily be integrated into the preference page by using the "Download missing binaries" button in the preference page. Alternatively, you can use 'Search in directory' for automatically searching the respective binaries in a provided local directory.
All additional files, like the reference genome, are already included within the workflows and dont have to be configured for running this test.
The provided workflows can then easily be imported into KNIME via *Import KNIME Workflow...* in the *File* menu.

## Variant Calling

The [variant calling workflow](https://github.com/ibisngs/knime4ngs/raw/master/KNIME4NGS_Test_VarCalling.knwf) covers all steps from raw read quality assessment to variant annotation. The following tools are required for this workflow:
* BWA
* Samtools
* [Picard] (https://broadinstitute.github.io/picard/)
* [GATK] (https://software.broadinstitute.org/gatk/download/)
* [SNPSift] (http://snpeff.sourceforge.net/download.html)

Binaries, which can't be directly downloaded by the "Download missing binaries" button in the preference page can be found through the the provided links. The workflow should be ready for execution right away. 

![](figures/VarCalling.png)


## Differential Expression

The [differential expression workflow](https://github.com/ibisngs/knime4ngs/raw/master/KNIME4NGS_Test_DiffExpression.knwf) initially creates a genome index used for read alignment.
Then, it iterates over RNA-seq data of 8 individuals, merges the read counts and uses the **DESeq** node to perform differential expression analysis. The following tools are required for this workflow:
* STAR
* FeatureCounts
* [DESeq] (http://bioconductor.org/packages/release/bioc/html/DESeq.html)

The workflow should be ready for execution right away.

![](figures/DiffExpression.png)







