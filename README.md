# TOXIper
Toxinotype assignment of *Clostridium perfringens* via ABRicate

## Dependencies
* ABRicate v1.0.1 (https://github.com/tseemann/abricate/tree/v1.0.1)and its dependencies (will be available using Conda)

## Usage
To trigger help/usage option
#### Help option
```
$ TOXIper.sh -h

This bash script assigns toxinotypes to C. perfringens genome assemblies using ABRicate v0.8.11 (type will be shown on stdout)
Dependency: ABRicate v0.8.11 with toxinCP database

Usage: /hpc-home/kiur/script/TOXIper.sh [options] FASTAFILE
Option:
 -h print usage and exit
 -a print author and exit
 -v print version and exit

Version 1.0
Author: Raymond Kiu Raymond.Kiu@quadram.ac.uk (2020)
```
#### Analyse a genome assembly
Toxinotype (e.g. A) will be printed on the stdout
```
$ TOXIper.sh CP-21.fna 
B
```

#### To save outcome into a file
Use > to save outcome into a new file, for example (can be any file name you like)
```
$ TOXIper.sh CP-21.fna > CP-21.toxinotype
```
