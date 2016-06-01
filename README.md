RNA Structural Bioinformatics Crash Course
-----------------------------------
Marcin Magnus (/my family name/@genesilico.pl)

(under development)

**Start a Google Docs and do the practicals!**

The sequence:

    GUUCCCGAAAGGAUGGCGGAAACGCCAGAUGCCUUGUAACCGAAAGGGGGAAU
	
Table of Contents
=================

  * [READ](#read)
  * [RNA structural bioinformatics](#rna-structural-bioinformatics)
    * [0\. Formats](#0-formats)
    * [1\. RNA sequence analysis](#1-rna-sequence-analysis)
    * [2\. RNA secondary structure](#2-rna-secondary-structure)
    * [3\. RNA 3D structure analysis](#3-rna-3d-structure-analysis)
  * [RNA 3D modeling](#rna-3d-modeling)
    * [Predict the structure using SimRNAweb/RNAComposer/MC\-SYM|MC\-Fold](#predict-the-structure-using-simrnawebrnacomposermc-symmc-fold)
    * [Modeling using restraint](#modeling-using-restraint)
    * [Assess the quality of your structure with mqapRNA](#assess-the-quality-of-your-structure-with-mqaprna)
    * [Calculate RMSD between A and B](#calculate-rmsd-between-a-and-b)
  * [RNA utils](#rna-utils)
    * [ModeRNA \- a program for comparative RNA modeling](#moderna---a-program-for-comparative-rna-modeling)
    * [ClaRNA](#clarna)
    * [RNA Bricks](#rna-bricks)
    * [NPDock \- protein\-RNA/DNA docking](#npdock---protein-rnadna-docking)
    * [QRNAS \- structure refinement](#qrnas---structure-refinement)
  * [Scientific software](#scientific-software)
    * [Biopython](#biopython)
    * [Pandas](#pandas)
    * [NumPy](#numpy)
    * [Matplotlib](#matplotlib)
    * [SciKit](#scikit)
    * [IPython Notebook (Jupyter)](#ipython-notebook-jupyter)
    * [PyMOL](#pymol)
  * [Utils](#utils)
    * [Python](#python)
      * [subprocess](#subprocess)
    * [Terminal](#terminal)
    * [Cluster](#cluster)
    * [Git](#git)
  * [More](#more)
    * [RNA motifs](#rna-motifs)
  * [References](#references)
  * [Books](#books)
  * [Notes](#notes)
    * [TODO](#todo)

Created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc.go)

# READ

Chapter #1 Introduction (by Michael Levitt) & #2 Modeling RNA Molecules (by Leontis & Westhof) & #5 Template-Based and Template-Free Modeling of RNA 3D Structure: Inspirations from Protein Structure Modeling of RNA 3D Structure Analysis and Prediction http://link.springer.com/book/10.1007%2F978-3-642-25740-7

# RNA structural bioinformatics
## 0. Formats

Which format to save:

- [ ] a sequence
- [ ] a secondary structure
- [ ] a structure.


## 1. RNA sequence analysis
a) What is a FASTA format? 

1. write the seq in the Fasta format

More: https://en.wikipedia.org/wiki/FASTA_format

b) **RFAM** database is a collection of RNA families, each represented by multiple sequence alignments, consensus secondary structures and covariance models (CMs). (http://rfam.xfam.org/)

1. Which RNA family the seq belongs to?
1. How many structures 
1. What members clan (CL00012) contains?
1. Download the alignment and view it in JalView

## 2. RNA secondary structure

Predict secondary structure for the sequence:

http://genesilico.pl/comparna/

Get ss from a structure (in the PDB format) 3E5C

http://link.springer.com/protocol/10.1007%2F978-1-62703-709-9_12
## 3. RNA 3D structure analysis
# RNA 3D modeling
## Predict the structure using SimRNAweb/RNAComposer/MC-SYM|MC-Fold
<http://iimcb.genesilico.pl/SimRNAweb/>
## Modeling using restraint
https://rmdb.stanford.edu/browse/
## Assess the quality of your structure with mqapRNA
<http://mqaprna-vm.dmz.genesilico.pl:8666/>
## Calculate RMSD between A and B


# RNA utils
## ModeRNA - a program for comparative RNA modeling
http://genesilico.pl/moderna/
## ClaRNA
## RNA Bricks
http://iimcb.genesilico.pl/rnabricks/

## NPDock - protein-RNA/DNA docking
http://genesilico.pl/NPDock/

## QRNAS - structure refinement
QRNA 0.2 - Quick Refinement of Nucleic Acids 0.2

Tutorial by Magnus https://docs.google.com/document/d/1ccbsZrnafBHJGEuXR2lvvMSh49VdTZMZfnyy0NFZxO8/edit

QRNA [RNA&DNA ONLY (incl. modified nts)

- adds missing atoms (esp. hydrogen)
- single-point energy calculations
- energy minimization in all-atom representation (Amber ff ONLY, implicit water, constraints possible)

https://docs.google.com/document/d/1ccbsZrnafBHJGEuXR2lvvMSh49VdTZMZfnyy0NFZxO8/edit

    $ ./QRNA -i pdbfile.pdb -o outfile.pdb
    It minimizes pdbfile.pdb and writes outfile.pdb every 100 steps. 
    All default parameters are used, which should be fine in most cases.

# Scientific software
## Biopython
The Biopython Project is an open-source collection of non-commercial Python tools for computational biology and bioinformatics, created by an international association of developers. It contains classes to represent biological sequences and sequence annotations, and it is able to read and write to a variety of file formats. It also allows for a programmatic means of accessing online databases of biological information, such as those at NCBI. Separate modules extend Biopython's capabilities to sequence alignment, protein structure, population genetics, phylogenetics, sequence motifs, and machine learning. Biopython is one of a number of Bio* projects designed to reduce code duplication in computational biology.

- [ ] read a seq.fa into biopython
- [ ] calc rmsd between two structures using biopython

More:

- https://en.wikipedia.org/wiki/Biopython
- http://biopython.org/wiki/Getting_Started

## Pandas
Pandas is a software library written for the Python programming language for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series. Pandas is free software released under the three-clause BSD license.[2] The name is derived from the term "panel data", an econometrics term for multidimensional structured data sets.

More:

- https://en.wikipedia.org/wiki/Pandas_%28software%29
- http://pandas.pydata.org/pandas-docs/version/0.18.1/10min.html

Practicals:

- [ ] make an dataframe, `df2` and run head(), tail(), and select a column

## NumPy
NumPy (pronounced "Numb Pie" or sometimes "Numb pee"[1][2]) is an extension to the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large library of high-level mathematical functions to operate on these arrays. The ancestor of NumPy, Numeric, was originally created by Jim Hugunin with contributions from several other developers. In 2005, Travis Oliphant created NumPy by incorporating features of the competing Numarray into Numeric, with extensive modifications. NumPy is open source and has many contributors.

More:

- https://en.wikipedia.org/wiki/NumPy
- http://www.numpy.org/
- https://docs.scipy.org/doc/numpy-dev/user/quickstart.html

Practicals:

- [ ] make an array of [2,3,1,0]
- ...

## Matplotlib
matplotlib is a plotting library for the Python programming language and its numerical mathematics extension NumPy. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits like wxPython, Qt, or GTK+. There is also a procedural "pylab" interface based on a state machine (like OpenGL), designed to closely resemble that of MATLAB. SciPy makes use of matplotlib. matplotlib was originally written by John D. Hunter, has an active development community, and is distributed under a BSD-style license. Michael Droettboom was nominated as matplotlib's lead developer shortly before John Hunter's death in 2012.

https://en.wikipedia.org/wiki/Matplotlib

Practicals:

- [ ] plot [2,3,1,0]
- ...

## SciKit
scikit-learn (formerly scikits.learn) is a free software machine learning library for the Python programming language.[2] It features various classification, regression and clustering algorithms including support vector machines, random forests, gradient boosting, k-means and DBSCAN, and is designed to interoperate with the Python numerical and scientific libraries NumPy and SciPy. scikit-learn is largely written in Python, with some core algorithms written in Cython to achieve performance. Support vector machines are implemented by a Cython wrapper around LIBSVM; logistic regression and linear support vector machines by a similar wrapper around LIBLINEAR.

- https://en.wikipedia.org/wiki/Scikit-learn
- http://scikit-learn.org/stable/

Practicals:

- run http://scikit-learn.org/stable/auto_examples/svm/plot_svm_regression.html#example-svm-plot-svm-regression-py

## IPython Notebook (Jupyter)
The IPython Notebook is now known as the Jupyter Notebook. It is an interactive computational environment, in which you can combine code execution, rich text, mathematics, plots and rich media. For more details on the Jupyter Notebook, please see the Jupyter website.

https://ipython.org/notebook.html
## PyMOL
- http://www.pymolwiki.org/index.php/Practical_Pymol_for_Beginners
- http://csb.stanford.edu/class/public/pages/sykes_pymol/pymol_info.html

Practicals:

- select a chain by clicking and from the cmd
- renumber a chain
- show a structure as cartoon and ribbon
- align two structures

# Utils
## Python
### subprocess
err = subprocess.call(cmd, shell=True)
## Terminal
The system console, computer console, root console, operator's console, or simply console is the text entry and display device for system administration messages, particularly those from the BIOS or boot loader, the kernel, from the init system and from the system logger. It is a physical device consisting of a keyboard and a screen, and traditionally is a text terminal, but may also be a graphical terminal. System consoles are generalized to computer terminals, which are abstracted respectively by virtual consoles and terminal emulators. Today communication with system consoles is generally done abstractly, via the standard streams (stdin, stdout, and stderr), but there may be system-specific interfaces, for example those used by the system kernel.

Practicals:

- [ ] show the contect of seq.fa file in your terminal
- [ ] change permission to execute to this file (just doesn't make any sense)
- [ ] install biopython/pymol from using terminal
- [ ] login to a remote machine using ssh keys
- [ ] mount a drive using sshfs
- [ ] download from the terminal this file http://files.rcsb.org/download/1XJR.pdb
- [ ] check the version of your system
- [ ] add this `~/bin/` to your (python) path and reload the file with a new variable
- [ ] grep a file...
- [ ] open a seq.fa in vim and quite ;-)
- [ ] take a look at the processes at your machine? (htop)
- [ ] write a simple bash script to run `cat seq.fa`
- [ ] go to your home and find `seq.fa`
- [ ] gzip `seq.fa`
- [ ] get the top of `seq.fa`
- [ ] get the bottom of `seq.fa`
- [ ] screen?
- [ ] diff?
- [ ] rsync?
- [ ] crontab?
- [ ] run mc and move to your home
- [ ] http://www.skamphausen.de/cgi-bin/ska/CDargs ?
- [ ] make an alias

https://en.wikipedia.org/wiki/System_console
## Cluster

magnus@peyote2:~$ qstat -u '*'

	for i in `seq -w 1 10`; do echo "../SimRNA -c config.dat -s 1gid.fas -S 1gid.ss -r 1gid_restraints_3_01.txt -E 10 -R $i -o 1gid+restraints_3_01_$i >& 1gid+restraints_3_01_$i.txt" | qsub -cwd -V -pe mpi 10 -l h_vmem=250M; done

## Git
Git (/ɡɪt/) is a version control system that is widely used for software development and other version control tasks. It is a distributed revision control system with an emphasis on speed, data integrity, and support for distributed, non-linear workflows.[9] Git was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.

<https://gitlab.genesilico.pl/Tutorials/git_crash_course> (private)

https://en.wikipedia.org/wiki/Git_%28software%29
# More

- https://ribokit.github.io/
- https://daslab.stanford.edu/resources/

## RNA motifs
https://en.wikipedia.org/wiki/Tetraloop

# References
Rfam 12.0: updates to the RNA families database. Eric P. Nawrocki, Sarah W. Burge, Alex Bateman, Jennifer Daub, Ruth Y. Eberhardt, Sean R. Eddy, Evan W. Floden, Paul P. Gardner, Thomas A. Jones, John Tate and Robert D. Finn Nucleic Acids Research (2014)  10.1093/nar/gku1063 

Gorodkin, J., & Walker, J. M. (n.d.). RNA Sequence , Structure , and Function : Computational and Bioinformatic Methods IN Series Editor.
# Books
**RNA 3D Structure Analysis and Prediction** Neocles Leontis, Eric Westhof 2012 http://link.springer.com/book/10.1007/978-3-642-25740-7

**RNA Sequence, Structure, and Function: Computational and Bioinformatic**, Methods Editors: Gorodkin, Jan, Ruzzo, Walter L. (Eds.) 2014 http://www.springer.com/us/book/9781627037082
# Notes
Seq in fasta format:

    >seq
    GUUCCCGAAAGGAUGGCGGAAACGCCAGAUGCCUUGUAACCGAAAGGGGGAAU

-------------------------------------------------------------------------------

Crystal Structure of the SMK box (SAM-III) Riboswitch with SAM

    >3E5C:A|PDBID|CHAIN|SEQUENCE
    GUUCCCGAAAGGAUGGCGGAAACGCCAGAUGCCUUGUAACCGAAAGGGGGAAU

http://www.rcsb.org/pdb/files/fasta.txt?structureIdList=3E5C

-------------------------------------------------------------------------------

The SMKbox riboswitch (also known as SAM-III) is a RNA element that regulates gene expression in bacteria.[2][3] The SMK box riboswitch is found in the 5' UTR of the MetK gene in lactic acid bacteria. The structure of this element changes upon binding to S-adenosyl methionine (SAM) to a conformation that blocks the shine-dalgarno sequence and blocks translation of the gene.

There are other known SAM-binding riboswitches such as SAM-I and SAM-II, but these appear to share no similarity in sequence or structure to SAM-III. http://rfam.xfam.org/family/RF01767#cite_note-pmid18806797-1


-------------------------------------------------------------------------------

Get clusters of 3e5c 

- http://ndbserver.rutgers.edu/service/ndb/atlas/stfeatures?searchTarget=ur0166&ftrType=nr&start=0&limit=0
- http://rna.bgsu.edu/rna3dhub/nrlist/view/NR_all_19088.1

-------------------------------------------------------------------------------

Secondary structure:

    GUUCCCGAAAGGAUGGCGGAAACGCCAGAUGCCUUGUAACCGAAAGGGGGAAU
    ((((((..((((.(((((....)))))....))))....((....)))))))) # 3E5C.pdb rnapdbee
    ((((((..((((.(((((....)))))....))))....((....)))))))) # mfold (-24.00) / 1. 

1. http://unafold.rna.albany.edu/results/9/16Jun01-09-40-08/16Jun01-09-40-08_1.b
## TODO

- use data from Rhiju to model any RNA

