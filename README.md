# Resequencing: 

TODO: Introductory Description

Table of contents
=================

  * [Overview](#overview)
  * [Manual](#manual)
    * [Running with SMRTAnalysis](#running-with-smrtanalysis)
    * [Running on the Command-Line](#running-on-the-command-line)
    * [Running on the Command-Line with pbsmrtpipe](#running-on-the-command-line-with-pbsmrtpipe)
  * [Advanced Analysis Options](#advanced-analysis-options)
    * [SMRTLink Resequencing Options](#smrtlink-resequencing-options)
    * [PBAlign Options](#pbalign-options)
    * [GenomicConsensus Options](#genomicconsensus-options)
    * [pbsmrtpipe Resequencing Options](#pbsmrtpipe-resequencing-options)
  * [Output Files](#output-files)
    * [PBAlign Output Files](#pbalign-output-files)
    * [GenomicConsensus Output Files](#genomicconsensus-output-files)
  * [Algorithm Modules](#algorithm-modules)
  * [Glossary](#glossary)

## Overview

![resequencing](https://cloud.githubusercontent.com/assets/12494820/11485866/7cd26f12-976a-11e5-8a22-fc76d70507b7.png)


##Manual

##Running with SMRTAnalysis

##Running on the Command Line

##Running on the Command-Line with pbsmrtpipe
###Install pbsmrtpipe
pbsmrtpipe is a part of `smrtanalysis-3.0` package and will be installed
if `smrtanalysis-3.0` has been installed on your system. Or you can [download   pbsmrtpipe](https://github.com/PacificBiosciences/pbsmrtpipe) and [install](http://pbsmrtpipe.readthedocs.org/en/master/).
    
You can verify that pbsmrtpipe is running OK by:

    pbsmrtpipe --help


## Advanced Analysis Options

## SMRTLink Resequencing Options

You may modify advanced analysis parameters for Resequencing as described below via SMRTLink.

| Module |           Parameter           |     Default      |  Explanation      |
| ------ | -------------------------- | --------------------------- | ----------------- |
| GenomicConsenus | Algorithm Name  | quiver  | Specifies the algorithm to be used by GenomicConsenus. Options are "quiver" and "plurality" |
| GenomicConsenus | Diploid mode (experimental)  | unchecked  | Enable detection of heterozygous variants (experimental) |
| GenomicConsenus | Minimum confidence  | 40  | The minimum confidence for a variant call to be output to variants.gff |
| GenomicConsenus | Minimum coverage  | 5  | The minimum site coverage that must be achieved for variant calls and consensus to be calculated for a site. |
| PBAlign | Algorithm options  | -minMatch 12 -bestn 10 -minPctIdentity 70.0  | List of space-separated arguments passed to BLASR |
| PBAlign | Concordant alignment  | checked  | Map subreads of a ZMW to the same genomic location |
| PBAlign | Consolidate .bam  | unchecked  | Merge chunked/gathered .bam files |
| PBAlign | Number of .bam files  | 1  | Number of .bam files to create in consolidate mode |
| GenomicConsenus | Hit policy  | 40  | Specify a policy for how to treat multiple hit random : selects a random hit. all : selects all hits. allbest : selects all the best score hits. randombest: selects a random hit from all best score hits. leftmost : selects a hit which has the best score and the smallest mapping coordinate in any reference. Default value is randombest. |
| GenomicConsenus | Min. accuracy  | 70  | Minimum required alignment accuracy (percent) |
| GenomicConsenus | Min. length  | 50  | Minimum required alignment length |


## PBAlign Options

## GenomicConsensus Options

## pbsmrtpipe Resequencing Options

## Output Files
## PBAlign Output Files

##GenomicConsensus Output Files

## Algorithm Modules

## Glossary

