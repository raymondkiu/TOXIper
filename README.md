# TOXIper
Toxinotype assignment of *Clostridium perfringens* via ABRicate. *C. perfringens* has 7 toxinotypes (i.e. A-G) based on the different combinations of toxin genes. A validated/published [toxin gene database](https://github.com/raymondkiu/TOXIper/blob/master/sequences) is included in this repository.

## Dependencies
* [ABRicate v1.0.1](https://github.com/tseemann/abricate/tree/v1.0.1) and its dependencies (will be available using Conda)

## Usage
### Set up ABRicate database for *C. perfringens toxin genes*
Please refer to this section in ABRicate github page: https://github.com/tseemann/abricate#making-your-own-database

### Help option
```
$ TOXIper.sh -h

This bash script assigns toxinotypes to C. perfringens genome assemblies using ABRicate v1.0.1 (type will be shown on stdout)
Dependency: ABRicate v1.0.1 with toxinCP database

Usage: ./TOXIper.sh [options] FASTAFILE
Option:
 -h print usage and exit
 -a print author and exit
 -v print version and exit

Version 1.1
Author: Raymond Kiu Raymond.Kiu@quadram.ac.uk (2020)
```
### Input - genome assemnbly
A *C. perfringens* genome assembly in multi-fasta format. One at a time. To give you an idea what a multi-fasta format is:
```
>Contig1
ATTCGCGAAAGGCCCCCCTTTG
ATGGGGTGTGCCCCCGGTGTGT
```
It will not work on bugs other than *C. perfringens* as genes will not be detected.

### To analyse a genome assembly
Toxinotype (e.g. B) will be printed on the stdout
```
$ TOXIper.sh CP-21.fna 
B
```
ABRicate BLASTn cutoffs will be set at default, which is minimum nucleotide identity >80% and minimum coverage >80%.

### To save outcome into a file
Use > to save outcome into a new file, for example (can be any file name you like)
```
$ TOXIper.sh CP-21.fna > CP-21.toxinotype
```
## License
[GPLv3](https://github.com/raymondkiu/TOXIper/blob/master/LICENSE)

## Issues
Please report bugs at the [issues page](https://github.com/raymondkiu/TOXIper/issues) so I can respond.

## Citation
- Please cite [this paper](https://doi.org/10.3389/fmicb.2017.02485) if you used the toxin sequence database for toxinotyping.
- Also cite [ABRicate](https://github.com/tseemann/abricate/tree/v1.0.1) as a dependency.

## Author
Raymond Kiu Raymond.Kiu@quadram.ac.uk
