Copied Template from Geoffroy Couteau in-case I lose it: https://geoffroycouteau.github.io/latex/

Instructions from Geoffroy
How to use it
Most of it is self-explanatory. The main file is main.tex. Setting \fullversion to 1 will switch to a format with smaller margins, while setting it to 0 recovers the default margins which are mandatory for submissions to most IACR conferences, such as CRYPTO and EUROCRYPT. Other toggles control whether the submission is anonymous, or whether todos should be shown.
I usually put all other LaTeX files in the directory tex_files. All standard packages and macro are in the file ZZ_header.tex, in the tex_files folder. If you plan to use the template, take a few minutes to scroll it to get a grasp of the many useful shortcuts (with standard crypto notations such as \Enc, \Dec, or useful math notations such as \F for F (field) \bit for {0,1}, etc).

I usually create a new LaTeX file for each new section, and input it directly in the main, like that:
```
\section{Introduction}
\label{sec:introduction}
\input{tex_files/01_introduction}
```
Using cryptobib
https://cryptobib.di.ens.fr/
Most references you will need can be found in the crypto.bib file. In many situations, downloading the file will suffice for your need, but sometimes the project might run for a longer time, and involve more people, in which case you might want the crypto.bib updates to be added automatically to your project. This can be done using submodules on git, or externals on svn. This is all well explained in the manual.
I usually add all missing citations in add.bib. To get them, I look for the paper on Google Scholar. The bibtex can be found under the “cite” icon (a quote sign).
The default template for citations is the following:
[venue_acronym]:[author_initials][year]

where:
venue_acronym is the standard shortcut for the name of the crypto conference or journal, e.g. EC for Eurocrypt, AC for Asiacrypt, EPRINT for ePrint, JoC for the Journal of Cryptology…
author_initials is the full author last name for papers with a single author (e.g. EC:Couteau19), the first three letters of each names for papers with two or three authors (e.g. C:CouHar20) and the first letter of each name for papers with four or more authors (e.g. CCS:BCGIKRS19).
year is the last two digits of the year (e.g. 21 for 2021).
