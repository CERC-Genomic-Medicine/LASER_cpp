# LASER

This package includes four programs for ancestry estimation and for preparing input files.

We also include example R codes (in the "plot" folder) to generate figures for results based on the HGDP reference panel. 
Color scheme and symbols for 53 HGDP populations are provided, which are consistent with those presented in Wang et al. (2014, Nature Genetics). 

## Installation

Before installing, the following software/packages are required:
- CMake 3.8+
- gcc
- gfortran
- openmp
- cget

Follow these steps to complete installation:

- Clone repository.
```sh
git clone https://github.com/CERC-Genomic-Medicine/LASER_cpp.git
cd LASER
```

- Compile and install.
```sh
cget install .
```

The compiled `laser` and `trace` executables will be located in `cget/bin` directory.



## Main programs for ancestry estimation

1. **laser** (**L**ocating **A**ncestry from **SE**quencing **R**eads) This program analyzes seqeuncing reads to estimate an individual's genetic ancestry in a reference ancestry space. Besides, the program also provide an option (-pca) to perform standard principal components analysis on genotype data. For details, please read the LASER_Manual.

2. **trace** (fas**T** and **R**obust **A**ncestry **C**oordinate **E**stimation) This program follows the same framework as LASER, but takes genotype data as input to place genotyped samples in a reference ancestry space. For details, please read the TRACE_Manual.

Pre-compiled executables of LASER and TRACE are placed in the current directory. Source codes of LASER and TRACE are placed in the "src" directory. Examples for running LASER and TRACE are placed in the "example" directory. User's manuals for LASER and TRACE are placed in the "doc" directory.

## Companion tools for preparing input data files

3. **vcf2geno** This program is a companion tool to covert a vcf file to a genotype data format taken by LASER and TRACE. Details of the genotype data format are described in the LASER_Manual. The executable, source codes, and examples  of the vcf2geno tool are in the "vcf2geno" directory.

4. **pileup2seq.py** This is a python script to prepare input sequencing data file for LASER. The program takes the pileup files from samtools (version 0.1.19), and output a matrix file that contains seuqencing reads mapped to a list to SNP loci. Details of the sequence format are described in the LASER_Manual. Examples and source codes of pileup2seq are in the "pileup2seq" directory.

## References

Wang et al. (2014). Ancestry estimation and control of population stratification for sequence-based association studies. Nature Genetics, 46: 409-415.

Wang et al. (2015). Improved ancestry estimation for both genotyping and sequencing data using projection Procrustes analysis and genotype imputation. American Journal of Human Genetics, 96: 926-937.


## Questions

If you have questions, please read the LASER_Manual or the TRACE_Manual first.
If the manuals cannot answer your questions, contact Chaolong Wang at chaolong@umich.edu or Daniel Taliun at dtaliun@umich.edu.


