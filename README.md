﻿# 102593_assignment

Hi there, very glad to meet you

This is a very little assignment to complete during the interviewing process. In essence it is about creating a very simple API around the data file that resides in the repo.

## Task

* Read the Data file in the repository
* Build three API endpoints that return (as JSON)
    * The aggregated number of proteins per sample sorted in descending order (data column `PG.ProteinAccessions`)
    * The aggregated number of peptides per sample (data colum `PEP.GroupingKey`)
    * result of a statistical test (e.g. a Welch-t-test, Students t-test, ...) per elution group (data column: `EG.PICMIDCharge`).
        * Construct the grouping based on the `R.FileName` Column:
        * There are files with a label `NewCol` in the file name, and files without. Those form the two groups to compare.

* Provide a markdown file along with the code containing:
    * Considerations / Thoughts for scaling the API to datasets of 500'000 x 500 and 100eds of concurrent users.
    * Were there specific reasons why you chose a specific approach / framework for this task?


## Expected Output

* Return your code and doc either via a github repository or an archive. You do not need to deploy it. 
* We value some instructions on how to run it locally

## Hints

* Important columns in the dataset:
    * `R.FileName` - unique identifier for a single sample
    * `PG.ProteinAccessions` - unique identifier for a protein
    * `PEP.GroupingKey` - unique identifier for a peptide
    * `EG.TargetQuantity (Settings)` - the measured abundance of a protein. Use this as value input to the test
