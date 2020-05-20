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
### Input
A *C. perfringens* genome assembly in multi-fasta format. One at a time.

### To analyse a genome assembly
Toxinotype (e.g. B) will be printed on the stdout
```
$ TOXIper.sh CP-21.fna 
B
```

### To save outcome into a file
Use > to save outcome into a new file, for example (can be any file name you like)
```
$ TOXIper.sh CP-21.fna > CP-21.toxinotype
```
## Author
Raymond Kiu Raymond.Kiu@quadram.ac.uk
