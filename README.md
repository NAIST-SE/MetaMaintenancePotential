# Research Artifact: The Potential of Meta-Maintenance on GitHub

https://github.com/NAIST-SE/MetaMaintenancePotential/

This is a research artifact for the ICSE'21 paper "**Same File, Different Changes: The Potential of Meta-Maintenance on GitHub**". This artifact is a data repository including a list of studied 32,007 repositories on GitHub, the results of the qualitative analysis for RQ2, RQ3, and RQ4, the results of the quantitative analysis for RQ5, and survey material for RQ6. The purpose of this artifact is enabling researchers to replicate our mixed-methods results of the paper, and to reuse the results of our exploratory study for further software engineering research.

## Contents
- `LICENSE.md` - [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
- `README.md` - this file
- `STATUS.md` - application of an artifact badge of available
- `obtained_repositories.csv` - a list of studied 32,007 repositories (ID and path)
- `paper.pdf` - the accepted paper
- `qualitative_analysis.xlsx` - results of qualitative analysis for RQ2, RQ3, and RQ4
- `family_samples.csv` - results of code similarity analysis for RQ5
- `survey.pdf` - survey material for RQ6

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
