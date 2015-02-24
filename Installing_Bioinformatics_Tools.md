# Bioinformatics Software
Brian High  
February 24, 2015  

## Languages, Environments and Tools

- Programming Languages
    * R: [Bioconductor](http://www.bioconductor.org/)
    * Python: [SciPy](http://www.scipy.org/), 
    [Pandas](http://pandas.pydata.org/), 
    [Biopython](http://biopython.org/wiki/Main_Page)
    * Perl: [BioPerl](http://www.bioperl.org/wiki/Main_Page)
    * Java: [BioJava](http://biojava.org/wiki/Main_Page)
    * Other: C, C++, etc.
- Development Environments
    * [RStudio](http://www.rstudio.com/)
    * [IPython](http://ipython.org/)
    * [BioJava3 eclipse](http://biojava.org/wiki/BioJava3_eclipse)
- Operating Environments 
    * [Bio-Linux](http://environmentalomics.org/bio-linux/)
    * [bioknoppix](http://bioknoppix.hpcf.upr.edu/applications/)
- [Other](http://en.wikipedia.org/wiki/Category:Bioinformatics_software)
[software](http://en.wikipedia.org/wiki/List_of_open-source_bioinformatics_software), 
[tools](http://www.ccmb.med.umich.edu/bioinf-core/tools), 
[websites](http://www.colorado.edu/chemistry/bioinfo/BioinformaticsLinks.htm) 
and [databases](http://www.hsls.pitt.edu/obrc/)

## Installing Software

- Free-standing ("binary") applications and utilities
    * Download from developer (or use package manager like 
    [brew](http://brew.sh/))
    * These may be graphical or command-line programs
- Scripts and packages
    * First install the language interpreter or environment
    * Install additional language modules, packages, or libraries needed
    * Package managers ([biocLite](http://www.bioconductor.org/install/), 
    [pip](http://en.wikipedia.org/wiki/Pip_%28package_manager%29), 
    [cpan](http://www.cpan.org/modules/INSTALL.html), etc.) may install 
    dependencies for you
    * You often install and run these from a command-line "shell" like 
    [Bash](http://www.gnu.org/software/bash/)
- System Administration issues
    * You may need administrative ("superuser") rights to install
    * You may need to move files or modify environment variables like `PATH`
    * You may need to use `git`, `svn`, or `hg` to pull from repositories

## Compiling Software

- Requirements
    * Programs written in languages like C and C++ must be compiled before use
    * If you can't download a "binary" of the program, you will have to compile
    * Mac users will need a development environment like 
    [XCode](https://developer.apple.com/xcode/)
    * Windows users may need a [GNU](https://www.gnu.org/) environment like 
    [Cygwin](https://www.cygwin.com/) or [MinGW](http://www.mingw.org/)
    * These include a compiler like [GCC](https://gcc.gnu.org/) and automation 
    tools like [make](http://www.gnu.org/software/make/)
    * A package manager like [MacPorts](https://www.macports.org/) can 
    automate the process
- Compilation steps are usually run from a command-line "shell" like 
    [Bash](http://www.gnu.org/software/bash/)
    * Usually these are listed in a README file (text, markdown, or HTML)
    * Can be as simple as: `./configure`, `make` and `sudo make install`
- `make` is a tool commonly used to automate compilation and installation
    * `./configure` prepares the [Makefile](http://en.wikipedia.org/wiki/Makefile) 
    and `make` processes it
- Tracking down and installing dependencies (libraries) may be tedious
    * Compile, fix errors, re-compile, fix errors, re-compile, etc.
    
## Examples from Research Papers: #1

What software tools will you need to reproduce results from these papers?

1. Leek, J. T. & Storey, J. D. [Capturing Heterogeneity in Gene Expression Studies by Surrogate Variable Analysis](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.0030161). PLoS Genet 3, e161 (2007).
2. Risso, D., Ngai, J., Speed, T. P. & Dudoit, S. [Normalization of RNA-seq data using factor analysis of control genes or samples](http://www.nature.com/nbt/journal/v32/n9/full/nbt.2931.html). Nature Biotechnology 32, 896–902 (2014).
3. Finak, G. et al. [OpenCyto: an open source infrastructure for scalable, robust, reproducible, and automated, end-to-end flow cytometry data analysis](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4148203/). PLoS Comput. Biol. 10, e1003806 (2014).
4. Zhong, Y. & Liu, Z. [Gene expression deconvolution in linear space](http://www.nature.com/nmeth/journal/v9/n1/full/nmeth.1830.html). Nat. Methods 9, 8–9– author reply 9 (2012).
5. Anders, S., Reyes, A. & Huber, W. [Detecting differential usage of exons from RNA-seq data](http://www.ncbi.nlm.nih.gov/pubmed/22722343). Genome Res. 22, 2008-2017 (2012).

These all seem to use R packages. Which ones? How do we install them?

## Examples from Research Papers: #2

What software tools will you need to reproduce results from this paper?

- McDavid, A. et al. [Data exploration, quality control and testing in single-cell qPCR-based gene expression experiments](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3570210/). Bioinformatics 29, 461-467 (2013).

This uses an R package. Do we install it with `install.packages` or `biocLite`?

## Examples from Research Papers: #3

What software tools will you need to reproduce results from this paper?

- Frazee, A. C., Sabunciyan, S., Hansen, K. D., Irizarry, R. A. & Leek, J. T. [Differential expression analysis of RNA-seq data at single-base resolution](http://biostatistics.oxfordjournals.org/content/early/2014/01/06/biostatistics.kxt053.full). Biostatistics kxt053 (2014). doi:10.1093/biostatistics/kxt053.

This study used a prototype version of an R package. What else is needed?

Some sample analysis code was provided. Great! What will we need to run it?

## Examples from Research Papers: #4

What software tools will you need to reproduce results from this paper?

- Hansen, K. D., Langmead, B. & Irizarry, R. A. [BSmooth: from whole genome bisulfite sequencing reads to differentially methylated regions](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC3491411/). Genome Biol. (2012).

This paper presents a "pipeline". How do we get it to work?

## Examples from Research Papers: #5

What software tools will you need to reproduce results from this paper?

- Amir, E.-A. D. et al. [viSNE enables visualization of high dimensional single-cell data and reveals phenotypic heterogeneity of leukemia](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC4076922/). Nature Biotechnology 31, 545–552 (2013).

From within what environment do we use viSNE? How do we access it?

## What about our RSEM example?

- [Using RSEM, a hands-on example](https://github.com/raphg/Biostat-578/blob/master/Using_RSEM.md)

The requirements are listed at the top of the article. How would we install them?

## What about our RSEM example?

Regarding data for the [example](https://github.com/raphg/Biostat-578/blob/master/Using_RSEM.md), Raphael posted three essential files in a Dropbox folder:

- [hg19.fa](https://www.biostars.org/p/1796/)
- [knownIsoforms](https://groups.google.com/forum/#!topic/rsem-users/oto_OJg5NcQ)
- [UCSC.gtf](https://groups.google.com/a/soe.ucsc.edu/d/msg/genome/kyk7AAm4R-M/9LkE-CRjzioJ)

[What](http://bioinformatics.oxfordjournals.org/content/22/9/1036.full) are they? [Where](http://genome.ucsc.edu/) did they come from? Why not [just](https://github.com/raphg/Biostat-578/blob/master/using_rsem_prep_input.sh) [get](http://genomewiki.ucsc.edu/index.php/Genes_in_gtf_or_gff_format) [them](http://hgdownload.cse.ucsc.edu/goldenPath/hg19/bigZips/) from [the](http://hgdownload.cse.ucsc.edu/downloads.html#human) [source](http://hgdownload.cse.ucsc.edu/goldenpath/hg19/database/)?


```bash
cd ./RSEM_test/Reference_Genome/
../../using_rsem_prep_input.sh
```

That [script](https://github.com/raphg/Biostat-578/blob/master/using_rsem_prep_input.sh) will download the three files from UCSC. A little extra processing is done to extract, convert, or rename the files.

## Example: Trinity and RSEM Test

Assuming you have already installed 
[bowtie](http://bowtie-bio.sourceforge.net/index.shtml) and 
[bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml), 
you can run this shell script to compile and test 
[Trinity and RSEM](http://trinityrnaseq.sourceforge.net/analysis/abundance_estimation.html).


```bash
#!/bin/sh

# Test Trinity and RSEM
mkdir -p ~/biotools/
cd ~/biotools/
git clone 'https://github.com/bli25wisc/RSEM.git'
cd ./RSEM/
make
make ebseq
export PATH=$PATH:~/biotools/RSEM
cd ../
git clone 'https://github.com/trinityrnaseq/trinityrnaseq.git'
cd ./trinityrnaseq/
make clean
make
cd ./sample_data/test_Trinity_Assembly
./runMe.sh
```

You should see a lot of verbose output. Did the test run okay?

## Example: Bowtie, RSEM, and Detonate

We have another [example script](https://github.com/raphg/Biostat-578/blob/master/detonate_test.sh) which tests:

- [Bowtie](http://bowtie-bio.sourceforge.net/index.shtml)
- [RSEM](https://github.com/bli25wisc/RSEM)
- [Detonate](https://github.com/deweylab/detonate)

Detonate requires [Blat](https://genome.ucsc.edu/FAQ/FAQblat.html).

The script assumes bowtie is already installed. The rest are downloaded and 
compiled. In each case, the compile command is simply `make`.

Read the script's comments to learn about other dependencies for compiling.


```bash
./detonate_test.sh
```