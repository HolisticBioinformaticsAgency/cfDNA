# cfDNA

### This is the beginnings of the pipeline for a CellFree DNA project.

There are some caveats:

It expects a folder of fastq files, with suitable names for processing later. This format is shown below, and needs an identical name.  I normally create these new names as symlinks in a folder called "fastqs" inside the project folder.

```
ls -s /fs02/vh83/raw_data/cfdna/AGRF_CAGRF220510607_H7VWLDRX2/gmDNA_H7VWLDRX2_CTACCGAA-AGACACTT_L001_R1.fastq.gz O3_gmDNA_R1.fastq.gz
ls -s /fs02/vh83/raw_data/cfdna/AGRF_CAGRF220510607_H7VWLDRX2/gmDNA_H7VWLDRX2_CTACCGAA-AGACACTT_L001_R2.fastq.gz O3_gmDNA_R2.fastq.gz
ls -s /fs02/vh83/raw_data/cfdna/AGRF_CAGRF220510607_H7VWLDRX2/ptimisation_2_cfDNA_H7VWLDRX2_CTACAATG-GTCAAGTC_L001_R1.fastq.gz O3_cfDNA_R1.fastq.gz
ls -s /fs02/vh83/raw_data/cfdna/AGRF_CAGRF220510607_H7VWLDRX2/ptimisation_2_cfDNA_H7VWLDRX2_CTACAATG-GTCAAGTC_L001_R2.fastq.gz O3_cfDNA_R2.fastq.gz
```
by default metrics are generated per target and across the panel using HsMetrics from Picard.  I normally create a padded interval file with 100bp of padding on each side of each region to use as the target file, while the covered.bed from agilent is used as the bait file.


TODO:

The config file needs to be edited to be specific to the inhouse slurm cluster at PeterMac.
Roll all software dependencies will be rolled into a singularity env to make it more portable



