# Silent Dropping of Non-Existent Columns in R Subsetting
This repository demonstrates a subtle bug in R related to subsetting data frames using character vectors. When you attempt to select columns that do not exist, R silently drops them without any warning or error message. This can make debugging quite difficult.

## Bug
The `bug.R` file contains the buggy code.  It attempts to subset a data frame using a vector of column names.  Some of these names are not actual column names in the data frame.

## Solution
The `bugSolution.R` file demonstrates a more robust method using `dplyr::select` to handle missing column names. This approach will throw an error if any of the specified columns don't exist, helping to catch the problem early.

This example highlights the importance of careful error handling and the use of packages like `dplyr` which provide more explicit error checking when working with R data frames.