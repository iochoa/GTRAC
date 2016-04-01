# GTRAC
GeneType Random Access Compressor

## Getting Started
### Install
The install the dependencies and the required code:
```bash
# Run the install file to download and install rsdic,TGC and GTRAC libraries
./install.sh
```

The shell script clones the following git repositories and installs them:

1. ![rsdic](): The library implementation of succinct bitvectors
2. ![TGC](): The TGC Compressor, which we use for VCF file handling and variant dictionary compression
3. ![GTRAC](): The GTRAC compressor implementation

### Run
You can run an example of the GTRAC compressor using the following command.
```bash
# Run GTRAC for the chromosomes mentioned in config.ini of the 1000GP project
./run -abceik
```
The shell script does the following thigs:

1. Downloads VCF and reference files (for chromosome 22, by default) corresponding to the 1000 Genome Project
2. Uses tools from **TGC** repo to process the VCF files and convert it into the $$(H,VD)$$ representation
3. Uses GTRAC compressor to compress the biinary matrix H  
e ToDO
