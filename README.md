# Research Artifact: The Potential of Meta-Maintenance on GitHub

https://github.com/NAIST-SE/MetaMaintenancePotential/

This is a research artifact for the ICSE'21 paper "**Same File, Different Changes: The Potential of Meta-Maintenance on GitHub**". This artifact is a data repository including a list of studied 32,007 repositories on GitHub, a list of targeted 401,610,677 files, the results of the qualitative analysis for RQ2, RQ3, and RQ4, the results of the quantitative analysis for RQ5, and survey material for RQ6. The purpose of this artifact is enabling researchers to replicate our mixed-methods results of the paper, and to reuse the results of our exploratory study for further software engineering research.

## Contents
- `LICENSE.md` - [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
- `README.md` - this file
- `STATUS.md` - application of an artifact badge of available
- `obtained_repositories.csv` - a list of studied 32,007 repositories (repository ID and path)
- `paper.pdf` - the accepted paper
- `qualitative_analysis.xlsx` - results of qualitative analysis for RQ2, RQ3, and RQ4
- `family_samples.csv` - results of code similarity analysis for RQ5
- `survey.pdf` - survey material for RQ6
- `blob.csv.zip` - a list of targeted 401,610,677 files including 27,994,587 seed files (SHA-1 hash of a blob, repository ID, filename extension, programming language)

## Details

### qualitative_analysis.xlsx

This is the results of our qualitative analysis using the following coding guides.

**coding guide for RQ2**
- *library* - a program that contains a collection of code used by applications
- *utility functionality* - a system software for controlling the operation of a computer, devices, etc.
- *configuration* - Configuration files
- *other* - mostly for header files or files containing version information

**coding guide for RQ3**
- *related* - There is an explicit relationship among repositories, e.g., one is a fork of another, their names are similar or identical, or because one mentions the other prominently in its documentation.
- *non-related* - On the other hand, many seed families do not contain any evidence to suggest that there is a connection among the repositories, apart from using at least one common file.

**coding guide for RQ4**
- *reference to a known origin* - For many repositories in our sample, the origin is obvious - this applies in particular to the various Linux variants. In those cases, changes that have been applied to seed files are often the same commits that have been applied to the origin.
- *library updates* - Library updates.
- *project-specific changes* - The most interesting case for meta-maintenance are project-specific changes which are not library updates or made in reference to a known origin.
- *tangled updates* - In case the commit history contained changes that could not easily be localized to the file under investigation, we applied this code.
- *other* - For change histories which did not fit any of the previous categories, we applied this code.


### family_samples.csv

The CSV file includes seed family samples.
Each line represents a variant `v` of a seed family.  Duplicate variants are excluded.

 - `strata` - the strata including the seed family.
 - `blob1` - the blob ID of the seed file.  The variants having the same `blob1` belong to the same seed family.
 - `loc` - the number of lines of the seed file.
 - `url` - GitHub link to see the variant file `v`.  
 - `commit` - the commit including the seed file in the repository
 - `head` - the revision analyzed in the paper
 - `modificationcount` - the number of commits that modified the variant file
 - `blob2` -  the blob ID of `v` in the `head` revision
 - `sha1` - the SHA-1 hash of the file content of `v`
 - `retention` - the value of `Retention_f(v, seed)` in the paper
 - `uniqueness` - the value of `u(v, the seed family members other than v)` in the paper

To calculate the retention and uniqueness, we have used a tokenizer `FileTokenizerMain` included in the [CodeHash Tool](https://github.com/NAIST-SE/CodeHash).


## Authors
- [Hideaki Hata](https://hideakihata.github.io/)
- [Raula Gaikovina Kula](https://raux.github.io/)
- [Takashi Ishio](https://takashi-ishio.github.io/index-en.html)
- [Christoph Treude](http://ctreude.ca/)
